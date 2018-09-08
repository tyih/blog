#iOS开发－KVO的奥秘
之前一直对KVO保持着一种神秘感，感觉好难的样子，这次看了这篇文章，希望填补一下脑子里面的空缺，能说出个一二三来，并能学以致用。

KVO(key-value-observing)是一种有趣的回调机制：某个对象注册监听者后，在被监听的对象发生改变时，会发送一个通知给监听者，以便监听者执行回调操作。

最常见的KVO运用是监听scrollView的contentOffset属性，完成用户滚动时动态改变某些控件的属性实现效果，如：渐变导航栏、下拉刷新控件等。

##使用
使用KVO的要求时对象必须能支持KVC机制－所有NSObject的子类都支持这个机制。

如渐变导航栏，我们为tableView添加了一个监听者controller，当滑动的时候，会计算当前的滚动偏移量，然后改变导航栏的背景色透明度。
...

KVO是一种非常便捷的回调方式，但编译器是怎么完成监听这个任务的呢？
苹果文档对KVO的实现描述：

	Automatic key-value observing is implemented using a 
	technique called isa-swizzling... When an observer
	is registered for an attribute of an object the isa 
	pointer of the observed object is modified, pointing 
	to an intermediate class rather than at the true 
	class ..

所以，当我们完成对tableView的监听后，编译器会修改tableView的isa指针，使他指向新生成的中间类。

解释：isa是一个Class类型的指针，用来指向类的类型，可以通过object_getClass方法获取这个值(正常来说，class方法内部的实现就是获取这个isa指针，但是在kvo中苹果对监听对象的这个方法进行了重写)

在OC中，规定了只要拥有isa指针的变量，通通都属于对象。上面的objc_object表示的是NSObject这个累的结构体表示，因此OC不允许出现非NSObject子类的对象(block是一个特殊的例外)

##苹果的黑魔法
根据苹果的说法，在对象完成监听注册后，修改了被监听对象的某些属性，并且改变了isa指针，那么我们可以在监听前后输出被监听对象的相关属性来进一步探索KVO的原理。为了保证能够得到对象的真实类型，使用object_getClass方法(class方法本质上是调用这个函数)，这个方法在runtime.h头文件中
...

经过实验发现，监听前后被监听对象的地址是一样的。
```
NSLog(@"%@, %@", self.class, super.class);
```
这是由于super本质上指向的是父类内存。

每一个对象占用的内存中，一部分是父类属性占用的；在父类占用的内存中，又有一部分是父类的父类占用的。isa指针指向的是父类，因此Son的地址从Father开始，Father的地址从NSObject开始，这三个对象内存地址都是一样的。

通过这个，可以猜到苹果文档中所提及的中间类就是被监听对象的子类。并且为了隐藏实现，苹果还重写了这个子类的class方法和description方法来掩人耳目。此外，我们还看到了新类相对于父类添加了一个NSKVONotifying_前缀，添加这个前缀是为了避免多次创建监听子类，节省资源。

##实现类似效果
...比较复杂

##总结
研究KVO的实现可以让我们对苹果的代码有更深层次的了解，这些知识涉及到更深层次的技术，探究他们对于我们开发视野有很重要的作用。

相对其它的回调方法，KVO的实现在创建子类、重写方法等方面内存消耗是巨大的，更加推荐使用delegate、block等回调方式，甚至直接使用method-swizzling来替换这种重写setter方式。

摘自[这里](http://www.jianshu.com/p/742b4b248da9)