#iOS Quick Tip: From Novice to Expert (转)
Bart Jacobs on Jul 29th 2013 with 5 comments

	Even though it’s possible to learn the essentials of 
	iOS Development in a weekend, it will take much 
	longer to master the craft. The question then is how 
	do you transition from a novice to an expert? In 
	this quick tip, I will provide you with a breadcrumb 
	trail that may help you on your way to becoming a 
	great iOS developer.

虽然,在一个惬意的周末学习IOS开发是可行的,但是呢,想完全熟练的掌握它可要花费n长时间.问题是,你怎样才能够从一个菜鸟变成老鸟?在以下简短的描述中,我会给你来点建议,帮助你尽快上路,成为IOS开发者的高手.


	1. Practice, Practice, Practice
	There are no shortcuts. This is something that I’d 
	like to emphasize before continuing, because it is 
	important to get rid of any illusions that might be 
	stuck in your head. You don’t become a skilled 
	developer if you only program on Sunday afternoons 
	between 4PM and 5PM…if the sun isn’t shining and 
	there’s nothing on television. Don’t get me wrong, 
	it may be fun to do so, but it won’t bring you much 
	closer to your goal of becoming an expert developer. 
	Apart from a few exceptions, most people need 
	practice -and lots of it. If you aren’t prepared to 
	put in the hours, then it’s better to revisit your 
	goals and ambitions. Become great at something you 
	love and the time spent practicing will be its own 
	reward.

没有捷径啊少年!继续讲下去之前我得提前说一下,因为,摒除任何能够速成的想法而去面对残酷的现实是相当重要的.如果你仅仅想在星期天下午的4点到5点之间来搞一下,你是不可能成为一个高手的...仅仅是因为不能出去玩或者是看不了<生活大爆炸>了.别耍我了,也许你觉得你已经花了一个小时的时间来做了,但是呢,那绝不会让你接近你想成为高手目标的一步.抛开一些例外,大部分人都需要练习.练习再练习,如果你不想花时间去做,那你就别想成为高手而继续当苦逼码农.花费时间以及精力去做你喜欢做得一些事情是成为高手的必经之路.

	2. Learn From Others
	One of the best strategies to improve your skills 
	and to adopt best practices is to learn from other 
	people’s code. This not only means browsingStack 
	Overflow, but also, and more importantly, libraries 
	or code snippets that are open sourced by fellow 
	developers.

一个提高你能力的最好的策略以及最有效率做练习的方式就是去学习别人的代码.这里不仅仅是说你去 Stack Overflow (栈溢出网站可是相当不错的网站哦)网站上去取经就够了,去学习少数大神的开源库以及它们的一些代码片段也是非常重要的.

	Whenever you dive into a library, such as 
	AFNetworking or Magical Record, it is key to not be 
	overwhelmed by the code you read. Chances are that 
	you don’t understand every line of code in these 
	libraries, but that’s not really the point. The 
	point is to look at the source code from a higher 
	level and learn as much as possible, such as naming 
	conventions, best practices, design patterns, etc.

一旦你深入到了一个库,例如 AFNetworking 或者 Magical Record,不要被那些晦涩难懂的巨量的代码所吓尿了,你不可能懂得这些库里面的每一行代码每一处私密的地方,但是呢,那不是学习的要点所在哦,真正需要学到的是,从一个更高的角度来尽可能的学习它们,例如一些常用的使用方法,设计优秀的地方,设计模式等等诸如此类.

	In addition to learning from other people’s code, it 
	is a good learning experience to create your own 
	libraries. Some time ago, I was developing an 
	application that uses Core Data as the data layer. 
	Instead of using Magical Record, I decided to create 
	my own library by exploring Magical Record and 
	recreating the pieces of functionality that I 
	needed. Not only did this result in a lean, agile 
	library, it also taught me a lot about the inner 
	workings of Magical Record.

除了去学习别人的代码之外,另一种好的学习经验就是创建你自己的库.long long ago, 我在开发一个应用程序时,那个...用到了Core Data作为应用程序的data层,而不是用Magical Record,我决定创建我自己的库,从Magical Record中寻求灵感以及提取出我自己想要的功能,最后呢,我不仅创建出了一个瘦小的灵活的库,而且,我还学习到了Magical Record中很多的核心设计方法.

	3. Don’t Copy and Paste
	This brings me to another key aspect of learning the 
	right way: don’t mindlessly copy and paste code. We 
	all use code snippets that we find on places like 
	Stack Overflow or Apple’s Developer Forums, but it’s 
	important to not mindlessly copy and paste the code 
	that you find on the web. By copying code that you 
	find, you don’t learn a thing. The greater danger is 
	that you don’t know what you’ve just added to your 
	code base. This might result in unexpected behavior 
	and it will make it very difficult to debug your 
	code later.

我的另外一个好的学习经验是:不要脑残的复制和粘贴别人的代码.或许我们都会从 Stack Overflow 或者 Apple's Developer Forums 中找到些代码片段来使用,但请不要随意的从网上下载代码然后无脑的进行复制粘贴.你用了你的不经过前额思考过的代码,你啥也不懂,而且,一个很大的风险是,你根本就不知道到底加了什么鬼东西到你的工程中,这个也许会出现各种奇葩的问题,而且,接下来,你得面对痛苦的debug过程,估计也搞不定的^_^.

	It may be tempting from time to time to quickly use 
	a code snippet that seemingly solves the problem 
	that you are working on, but I strongly urge against 
	this practice. Read the code, understand what you 
	are adding into the code base, and, possibly, 
	customize the solution to your needs.

一次又一次的快速的无脑的使用了别人的代码片段且貌似解决了你当前的难题,这是如此的吸引人啊.但我强烈的反对这种方式,研究那些代码吧,至少你得知道把什么东西加进了你的工程中,最好的就是修改别人的代码以及定制出你自己需要的解决方法.

	It goes without saying that this doesn’t apply to 
	libraries or frameworks that are actively 
	maintained. If you had to go through Magical Record 
	before you’d be able to use it in your project… I’m 
	sure you understand the difference. Use your common 
	sense.

这可不是说叫你抛弃那些正在更新和维护的(第一方提供的)库和框架.[一句话翻译不了了,英语水平菜,理不清语法结构了-_-!!!]...我能确定,你将会体验到不同点,平时怎么整的就怎么整吧.

	4. Patterns
	Cocoa and Objective-C are in many ways very 
	different from other programming languages and 
	environments. This means that they have their own 
	patterns and best practices. I’m sure that you’re 
	already familiar with a few common patterns, such as 
	delegation and notifications. However, there are 
	many more patterns that can help you during your 
	development, such as the singleton, observer, and 
	command patterns. The Cocoa Fundamentals Guide gives 
	you a nice overview of the most common patterns in 
	Cocoa.

Cocoa 和 Objective-C 在某些地方,与其他的编程语言有着很大的差异哦,这意味着,它们都有着它们自己的一种模式和一种最适合自己的编程方式.我相信,你已经对一些常用的设计模式如代理和通知模式有所了解.然而,还有着其他的一些(设计)模式能够帮助你开发,诸如单例.观察者.和指挥者模式.这本书 Cocoa Fundamentals Guide 能给你一个较为全面的关于Cocoa中使用到的一些设计模式的指导.

	5. Know Your Tools
	Becoming a great developer isn’t only about understanding the language and the frameworks. It is just as much about working efficiently with the tools that you use day in and day out. For iOS development, this means Xcode and possibly other tools, such as PonyDebugger andCharles.

了解了语言特性以及各种框架就能成为高手吗?想得美呢.你还得每天琢磨着怎么超高效的运用各种工具.对于开发IOS来说,这意味着要用好Xcode,还有其他的一些工具,比如PonyDebugger和Charles.

	If you’d like to learn a few extra tricks, you may be interested in a previous quick tip that I wrote about this topic.

你不想学一些额外的编程技巧吗?这样的话,也许,你会对我之前写过的一些快速提示感点兴趣.

	6. Stay Up To Date
	Even if you can’t attend Apple’s yearly developer conference, WWDC, it is a good idea to browse the numerous session videos and watch the ones that spark your interest. The presentations are usually given by the engineers that work on the technologies covered in the session, which gives you detailed information and instructions about how to use them. It is also a great way to quickly get up to speed with those technologies.

你不能参加苹果每年一度的开发者大会?别急,那就去看大量的会议视频吧,那也是能够拓宽你的视野的.你能得到很多的益处,那些都是各种领域内牛逼的工程师所免费赠送的^_^,你能从里面得到很多的最新的信息,以及帮助你怎么去用他们.这可是一种让你赶上日新月异的科技的一种技巧哦.

	There are many excellent developers that regularly write about their craft, such as Matt Gemmell, Aaron Hillegass, and Mike Ash. You can find a more extensive list in a previous post I’ve written for Mobiletuts+.

一些巨牛逼的开发者,经常会写写关于他们牛叉的工作的,如Matt Gemmel.Aaron Hillegass 和 Mike Ash,最近我已经把那份详细的变态人物列表分享在了Mobiletuts+网站上,来捧捧场吧.

	Bonus: Learn Other Languages
	I have noticed that my overall understanding of software development has improved significantly by learning new languages or working with new frameworks. The advantage of this approach is that you don’t limit your view of what is possible to the language that you are most familiar with.

我注意到了哦,我对于软件开发的综合能力,随着我去学习新的语言和使用新的框架而得到了显著的提升.也没想的那么容易,关键就是你不能够限制了自己的视野,不要把自己限定死在一种你最熟悉的开发语言中.

	I recently dipped my toes in Ember.js and learned that the creators, Yehuda Katz and Tom Dale took inspiration from Cocoa. The implementation of the MVC (Model-View-Controller) pattern of Ember.js is a bit unconventional for a JavaScript framework, but it is not that surprising if you are familiar with Cocoa.

最近我染指了Ember.js,他的创建者 Yehuda Katz 和 Tom Dale 可是从Cocoa开发中得到的灵感哟.这个MVC设计的实现对于JaveScript 框架来说可是很奇葩的(非传统的),但是呢,如果你熟悉Cocoa,那也没啥了不起的.

	There is no “best” language to write software in as they all have their pros and cons. The nice thing, however, is that they are all a little (or a lot) different and it’s those differences that makes learning new languages interesting and eye opening. Ruby, for example, was a real eye opener for me in terms of writing DRY (Don’t Repeat Yourself), readable, and clean code.

编写软件可没有什么最好的语言,每种语言都有其擅长的方面.好语言呢,就是那种它们只有一点点不同,然而就是这点点不同,让它学起来超级带感以及开阔视野.例如,Ruby,在编写DRY(别重复你自己),可读性和清新的代码方面令我大开眼界.

	Conclusion
	If you don’t want to put in the hours to become a better programmer, then you may want to reconsider why you wanted to become a programmer in the first place. However, if you get excited about a new library or tool that can help you in your development, then you probably won’t have a problem improving your skills over time. You really have to love what you do to become good at it and I think this is especially true for programming. No matter what people tell you, you won’t become an expert developer overnight, but I promise you that your skills will improve if you keep learning and beating on your craft.

如果你不想花费时间用在刀刃上一天到晚就知道dota.DNF.英雄联盟啊,你就得重新想想你能成为牛逼的开发者么?如果,一个新的库或者工具能够帮助你开发,你还乐于去使用它学习它,提升能力就指日可待.你真的需要喜欢上自己要做的事情,只有这样你才能真正的提高自己.不管别人怎么告诉你,你都不可能靠一个晚上就变成老手,但是,我知道,只要你能够坚持下去,你的能力一定能够得到提升!