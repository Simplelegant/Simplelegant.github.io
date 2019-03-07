---
layout:     post
title:      "游戏项目总结"
subtitle:   ""
date:       2019-3-7 18:54:04
author:     "Simpleelegant"
header-img: "img/post-bg-newstart.jpg"
tags:
    - 游戏开发
---

 <center>游戏项目总结</center>
 做出游戏来一直是我的梦想，正是因为这个原因我如此痴迷IT，从大学毕业到研究生阶段做过一些游戏，下面就挑3个来说吧。
 1.第一个是用汇编语言实现的贪吃蛇，为什么要选这个为第一个呢，因为当时大二的时候很想知道计算机的图像界面究竟是怎么实现的，接触了汇编才发现能够直接操作显存来显示图像很爽快。所以就做了这么一个游戏哈哈。
 ![training](https://simplelegant.github.io/img/blog-game-1.jpg)
 2.第二个是用MFC实现的俄罗斯方块，虽然MFC已经过时了但是当时看了《深入浅出MFC》后真的很震撼框架的消息机制，于是就写了个俄罗斯方块顺带练习了下C++和面对对象编程。
 ![training](https://simplelegant.github.io/img/blog-game-2.jpg)
 3.第三个是一个3D大游戏哈哈，用OGRE+CEGUI实现，大概写了半年吧，年轻的时候总是很喜欢开源的东西故选择了OGRE。当时写的开发日志如下：

> 2015
1.15-2.3 阅读ORGE官方文档                    
2.4 阅读OGRE官方教程
2.5 编译OGRE                                                  
2.6-2.7 完成第一版游戏框架搭建
2.11完成 菜单 游戏 暂停功能的实现
2.12完成镜头移动 人物行走基本功能
2.13完成第三人称摄像头改进
2.14完成地形跟随技术
2.15研究Sample_character
2.16研究Sample_character
2.23-2.26 基本完成RoleControl类的实现
 It's a big step.之前的方案特别凌乱，这样将主角封装在一个类之中使的实现相当优雅。
3.2-3.7 修复RoleControl的BUG,程序终于跑了起来。
3.9-3.11 研究IntermediateTutorial3，即鼠标拾取。
3.12     修改IntermediateTutorial3，使适合于目前版本的OGRE && CEGUI。
3.14    完成鼠标拾取。
3.15-3.18 研究IntermediateTutorial 4-7
3.19 终于可以让人物做其它动作了
3.20 研究Particle System粒子系统
3.21 实现粒子系统在游戏中的加载
3.22 初步实现战斗系统
3.24 解决战斗系统中的BUG
3.25 实现点击按键使用技能以及技能CD
3.26 修复技能CD错误的BUG,原来是逻辑错误，每次定时器都重启了，同时初步完成了指定性技能。
3.27-3.31 太忙了~~
4.1  重温了一遍CEGUI基本机制
4.2 完成CEGUI基本框架
4.3 突然发现这个框架的实现是基于旧版本CEGUI的，Dame it!
4.4 重写CEGUI框架，有了这个框架之后代码结构清晰多了
4.5 研究如何把天龙八部里面的素材用在自己的项目里，发现好麻烦啊
4.6 继续研究如何给天龙八部的mesh加载material
	main!!!
   终于想到了一个还算不错的游戏故事，暂时命名为 回家的诱惑。
   胃王大神给主角下了一道魔咒，在兰州城打听之后得知这道魔咒必须先回到临洮从南坪山上挖一些洋芋，挖完之后得知还必须去渭源采集一些渭河水，采集完之后知道回到家用渭河水熬制成火锅汤煮上洋芋就可以解除了。主角只好从兰州出发跋山涉水踏上了解除魔咒之旅。。。
   小西湖堵车 路被堵住了，只有战胜车王才能继续前行
   七道子梁遇上强盗
   南坪山上战胜土豆神才能踩得集万物之精华的洋芋  
   渭源战胜渭河神才能取渭河水
   最后在临洮吃了火锅解除了魔咒激怒了胃王，它从天而降，战胜胃王游戏结束！！
4.7 今天好累啊，游戏内可以显示对话框了
4.8 - 4.12 阅读《OGRE3D游戏开发框架指南》，为正式开始做游戏做准备
4.13 - 4.16 研究如何实现装备栏
4.17 了解了如何把其他的库集成进入自己的引擎，并初步尝试引擎的FMOD音频库集成
4.18 完成引擎的FMOD音频库集成，成功编译Lua5.3,成功编译物理引擎ODE
     新想法：先做一个3D格斗类游戏，之所以做这个决定是因为这样可以很好的熟悉一下新集成的FMOD和ODE引擎，游戏性很强的战斗系统离不开酷炫的3D音频效果和酣畅淋漓的物理引擎所提供的打斗场面，同时格斗对手的AI可以很好的熟悉一下LUA，其实这就是为RPG打基础。要是现在直接入手RPG未免工程量太大没有重点游戏没什么特色。
5.3 前段时间忙于复习考试开发基本停滞，终于弄出了可以随着分辨率变化的layout,只需把UDim中的offset设为0,仅仅用scale来设置窗口的位置。
5.5 终于找到了一种加载地形的时候显示载入图的方法！！！
5.7 改进了上一种框架，这次首先加载载入图，然后载入数据。
	ProgressBar可以使用了，哈哈，接下来物品系统。
5.8 研究CEGUI的DragDropDemo,打算用这个作为装备栏的雏形。
5.9 用CEED绘制了一个装备栏的layout。
5.10 终于发现了让layout自适应分辨率的好办法，在CEED中不要按下Absolute Resizing&&Moving Deltas。这样制作出来的窗口都是父窗口的缩放。
5.11 完成物品栏代码的初步实现。
5.12 可以在游戏中显示物品栏了。
     在游戏主界面中添加了一个现实物品栏的按钮。 
5.15 解决了在暂停菜单中显示完东西回到游戏崩溃的BUG
     把主界面的代码从GameState中抽取出来封装成了GameMainWindow类，逻辑更加清楚
     初步完成了物品拾取的代码，点击物品从场景上消失，加入物品栏中。
5.16 发现了上一版本装备栏的BUG,没有Slot直接把DragContainer拖动导致初始位置的DragContainer被拖走丢失。
     重绘装备栏。解决了上一个BUG。
     发现了物品拾取的BUG,未删除拾取的物品只是简单的隐藏了导致在相同位置还可以拾取。
5.17 CEGUI支持中文显示了。
5.18 研究了下LUA在游戏中的运用。
5.19 研究了下OGITOR,熟悉了基本操作，现在可以把天龙八部中的模型导入到OGITOR中了，开始了场景的制作。
5.20 绘制了新手村lanzhou_city的部分场景。
     发现了一个寻找mesh是使用什么material的好办法，把mesh加载进程序里边，然后看log就可以发现是使用了什么material,会提示Can't assign material 农村墙 to SubEntity of rural_qiang01#1 because this Material does not exist. Have you forgotten to define it in a .material 这样的信息。
     未解决问题：
     1.SkyX类型的天空无法在游戏中显示。 
5.21 完成了新手村场景的绘制。
5.23 知道了天龙八部的人物模型由好几部分组成，美工已经调整好了坐标，只需绑定到同一个节点即可。
5.26 可以给天龙八部的人物模型加载纹理了。
5.27 重新封装LeadingRole为适配天龙八部模型做准备。
5.28 为适配天龙八部骨骼修改OGRE源代码并编译，编译成功但是dll有问题。 
procedure entry point ?Ogre_InterlockedDecrement64@InterlockedCompareExchange64Wrapper@Ogre@@SA_JPC_J@Z could not be located in OgreMain_d.dll
5.29 昨天编译的是OGRE1.10分支的代码，怪不得有问题，现在重新编译1.9的代码。
5.30 初步解决编译问题，编译源代码的时候同时编译了boost,因为地形加载使用了多线程，最初只编译了OgreMain_d.dll,放到源程序中不行，显示procedure entry point ?Ogre_InterlockedDecrement64@InterlockedCompareExchange64Wrapper@Ogre@@SA_JPC_J@Z could not be located in OgreMain_d.dll。最后发现由于OGRE代码变化需要编译所有的DLL。
用boost1.58重新编译了PagedGementry。
5.31 下载了最新的Ogre1.9重新编译了所有文件，修改了GameApp依赖的OGRE代码为最新的代码，新的程序在F:\Ogre1.9\sdk\Game\Debug文件夹下，将新生成的程序和新生成的dll放在一起程序运行了！！！
    修改了OGRE源代码SkeletonSerializer::readAnimationTrack，可以加载天龙八部的动作了。
6.4 解决了天龙的模型只有身体运动的BUG，原来是把其他几部分的动作在Update里面没有更新。
重新编译了OgreMain_d.dll 和 OgreXMLConverter_d.exe，可以解析天龙的mesh和skeleton了。
了解了天龙的动作加载流畅，可以把武器挂载到骨骼上边了。
开始完善LeadingRole中的setupAnimations和updateAnimations，增加了一个新函数linkNewSkeleton,用来把包含动作的骨骼挂载到主角身上。
6.9 决定先写一个简单的动作系统，目前只加载自身的和0_男空手战斗的动作。
    由于主角由6部分组成，设置起来比较麻烦，写了一个内部类Animations把6部分的动作封装了起来。
    完成了setupAnimations，setupAnimations，setAnimations，但是有BUG.
7.4 期末考试结束了，休息了2天开始游戏制作了，之前遗留了做完动作之后恢复不到最初站立动作的BUG，于是从各skeleton中找站立的Animation，未找到。
    写了动作添加流畅：
增加新动作步骤
1.调用linkNewSkeleton函数将动作相关的骨骼链接进来
2.NUM_ANIMS + 1
3.AnimID中增加新动作名称
4.animationsName中增加新动作名称
5.调用setAnimation函数使用动作
7.5 终于找到了空手站立01，藏在4_男空手非战斗.skeleton中！！！但现在的问题是做完一个动作后依旧保持原动作，及时设置了回到站立动作。
7.6 完美解决动作滞留不恢复站立问题，原来是动作权重搞的鬼，现在引入了动作淡入淡出系统，淡入的时候权重为1，淡出的时候权重为0!!!现在感觉动作感流畅多了！！！Awesome!!!
 ![training](https://simplelegant.github.io/img/blog-game-3.jpg)