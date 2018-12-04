# 《计算机程序的构造和解释》---SICP学习记录
>> ![](https://img.shields.io/badge/language-Scheme-orange.svg) [![MIT license](https://img.shields.io/dub/l/vibe-d.svg)](https://github.com/Perry961002/Learning-notes-of-SICP/blob/master/LICENSE)

## A language isn’t something you learn so much as something you join.

<p align="center">
  <img src="http://groups.csail.mit.edu/mac/classes/6.001/abelson-sussman-lectures/wizard.jpg" alt="SICP"/>
</p>

## 为什么SICP那么重要？

从很多方面来看，SICP 都是一次革命。其中最为重要的是，它大幅提升了计算机科学专业入门课程的内容门槛。在 SICP 之前，计算机科学的第一门课程里几乎总是充斥着与学习编程语言相关的内容细节。SICP 完全与之相反，它更多地站在`全局角度思考编程的整体过程`，`远离编程语言的具体细节`。它将注意力重点放在了`抽象的核心思想`之上 - `从特定问题直至构建软件工具`，帮助你探求一般性的规律。SICP 大量使用了`『函数即数据』（functions as data）`在这一思想 - 一种在初始阶段难以理解和学习，但是一旦掌握之后便会得心应手的编程模式。（在初等微积分教学中，采用了同样的教育模式，即在开始阶段，哪怕你的数学功底异常扎实。学习过程也会比较艰难。）就在其它许多主题相似的课程还未谈到一个编程范式的时候，SICP 已将`三种不同的编程范式（函数式编程、面向对象式编程以及声明式编程）`巧妙地融入了一门计算机科学的入门课程之中。

SICP 的另一个创新之处就在于，它选择了 `Scheme` 作为教学语言。那个时候，绝大多数的计算机科学入门课程都在使用当时的热门编程语言：从 Pascal 到 C、C++、Java 以及 Python。Scheme 在工业界从没有大范围使用过，但是，对于计算机科学导论而言，它的确是一个完美的选择。一方面，Scheme 有`一套可用来表示任何对象的非常简单统一的符号系统`。一般情况下，其它编程语言会用一种符号表示变量赋值，另一种符号表示条件执行，两到三种符号表示循环，还有其它的符号用来表示函数调用。很多讲授这些编程语言的课程至少会花费一半的时间用于学习这些符号。在伯克利的 SICP 课程中，我们大约只需一个小时的时间就可以把所需的这些符号全部学完。在这一学期的剩余时间里，我们集中精力学习计算机科学核心思想和方法，而不是编程语言的语法。当然，尽管 Scheme 语法非常简洁，其功能却是多才多艺。`Scheme 不仅可以帮助我们体验三种不同的编程范式，而且，更为特别的是，它还让能让我们查看面向对象的编程究竟是如何实现的`。正是因为这个原因，对我的学生来说，那些 OOP 语言既不神奇也不陌生。由于 Scheme 是 Lisp 语言的一个分支，所以它能够游刃有余地将函数作为数据对待。与那些常见的专业编程语言相比，Scheme 更像是一个剥离了华丽外衣的原生编程工具。Abelson 和 Sussman 教授在他们的计算机导论课程中采用 Scheme 几乎就是一项勇敢的壮举。他们认为，`一旦你了解和掌握了这一思想，当然，这也是我的个人亲身经历，学习其它编程语言将不再是一件难事，充其量也就是一个周末的付出而已`。我告诉我的学生，`『那些你在工作中将会经常用到的语言或许还没有出现呢，所以我们恐怕无法给你们讲解它们。与之相反，在这些语言出现之前，我们必须教会你们如何学习一门新的编程语言。』`

最后，SICP 在看待大学新生从这门课程中取得的收获上始终保持积极乐观的态度。通常情况下，设计构建编译器可能更适合经验丰富的高年级学生，但是在 SICP 课程中，这项要求是必须的。SICP 这本教材的文字并不便于阅读 - 缺乏现代课本具有的排版风格 - 为了帮助学生在短注意力周期的条件下，保持他们兴趣而特意设置的侧边栏、彩色文本框以及照片等。没有冗余的课后练习，`每一项练习讲授一个重要的新思想`，`每一段话都非常重要`。SICP 喜欢使用一些『大』概念，但是在你仔细阅读之后，总能得到回报。

统计显示，SICP 风格的课程一直以来都属于少数派。但是这本书的影响力已经远远超过了一般范围。SICP 激励了很多后续的作者，他们非常渴望能够达到 SICP 的水准。采用 Scheme 作为教学语言已经扩展到了从中学到研究生院范围。即使在一些主流的计算机课程中，尽管更多侧重面向对象的编程，但是也开始越来越重视编程范式。`计算机科学这门专业应该更多地关注思想、应用环境以及计算的社会影响，而不是完全依赖编程实践或技巧`。

SICP 作为一本入门级计算机科学教材，其资历已经非常深厚了。迄今为止，SICP 已经出版超过了25年，目前来看，还没有停止印刷的打算。计算科学一直在不断地向前发展，从大型主机到个人电脑，直至移动互联网的出现。但是这些深藏在变化之中的那些基本思想始终未变，它们早已完整地包含在了 SICP 中。

我从 1987 年开始教授基于 SICP 的课程。这门课程随着时间的变化也在不停的修订。我已经为其添加了有关平行计算、并发控制、用户界面设计以及客户端/服务器技术等新内容。但是总体结构和内容没有任何变化。大约每过五年时间，我们的一些老师就会提出建议，这门课程采用的编程语言应该使用 X 语言替代。每次遇到这种情况，我就说，`『如果有谁能用这门语言写出世界上最好的编程教材，我们再做决定不迟。』` 而且，迄今为止，我们每一次的投票结果显示，SICP 课程应该保持原样。你们很快就会知道，这门课程是否会在我退休之后继续存活下来。

备注: 伯克利最新的计算机科学专业入门课程采用的编程语言是 Python。包括课程讲义在内，其内容与形式依然遵循和保留了 SICP 的主要特色。）

近一段时间，麻省理工学院由于重新设计了计算机科学与电子电气工程系的低年级系列课程，致使这一讨论变得异常尖锐。一些来自麻省理工学院之外的人将这次对课程的重新设计描述为『麻省理工决定切换至 Python，』 但是这不符合实情。麻省理工的真实决定是，从一种以主题为中心的课程设置模式（编程范式，然后是电路，然后是信号处理，然后是架构设计）转向另一种以应用为中心的课程设置模式（让我们一起来构建一个机器人，让我们一起来构建一个移动电话）。他们课程中的每一项内容都需要重新组织。编程语言的选择只是其中最小一项。这种新的方式给教学工作带来了很多困难和挑战。举一个例子：每一门课程都要求两个专业（计算机科学与电子电气工程）的老师紧密合作。或许一段时间之后，这种应用导向的教学模式将会引发一场就像 SICP 一样影响深刻的革命，但是目前看来，这场革命还没有发生。

在我的个人经历中，很少有学生在他们还在学习 SICP 这门课程的时候，表达他们对这门课程感谢之词。但是在一项针对所有计算机系学生的调查中，SICP 却是最受欢迎的课程之一，而且，经常有不少毕业许久的学生来拜访我，或者给我发来电子邮件，他们告诉我说，这些当他们还是学生时看似毫无用处的『象牙塔』概念，正在被实际应用到他们的具体项目之中。这让我们似乎觉得，谷歌公司基于函数式编程思想的数据并行处理技术 MapReduce 的发明，已经协助我们消除了『象牙塔』这一名声。

作者：Brian Harvey，计算机科学教育创新者，退休前在加州大学伯克利分校专职从事教学工作。

原文：[Why Structure and Interpretation of Computer Programs matters](https://www.cs.berkeley.edu/~bh/sicp.html)

## 视频地址

- [中译版视频专辑列表（优酷）](https://v.youku.com/v_show/id_XNTEzMDAyMTU2.html?f=18958522)

## 配置环境

- 采用了Chez Scheme作为解释器, 从[这个链接](https://www.scheme.com/download/)下载安装并配置环境变量, 这里提供了[Scheme的中文入门教程](https://github.com/DeathKing/yast-cn), 对函数式编程有兴趣的话可以去读一下[这一篇文章](https://github.com/justinyhuang/Functional-Programming-For-The-Rest-of-Us-Cn/tree/master)

- 到这里就可以在DOS环境下进行程序编写, 但为了方便可以使用VS Code
    - [VS Code下载](https://code.visualstudio.com/), 安装之后为VS Code扩展`Code Runner`和`vscode-scheme`插件

    - 在VS Code的设置中搜索`code-runner.executorMapByFileExtension`, 在最后一行追加内容`".scm": "scheme"`, 安装好后重启一下VS Code这样就能在右上角看见一个三角形了，打开文件点击就能编译执行

    - 现在还不能在终端中输入命令观察效果, 解决方法是依次打开: `文件>首选项>设置>用户设置>拓展>Run Code Configuration`, 找到 `Run In Terminal` 打上勾, 这样运行的程序就会运行在集成控制台上

## 案例和习题代码

- 如果代码中有错误或者有疑惑, 欢迎通过[Issues](https://github.com/Perry961002/Learning-notes-of-SICP/issues)或者邮箱Perry961002@163.com联系

| 章节(Chapter) |  01  |  02  |  03  |  04  |  05  |
|:-------------:|:----:|:----:|:----:|:----:|:----:|
| 案例(Example) | [Code](https://github.com/Perry961002/Learning-notes-of-SICP/tree/master/Chap1/example) |  [Code](https://github.com/Perry961002/Learning-notes-of-SICP/tree/master/Chap2/example) | --- | --- | --- |
| 习题(Exercises) | [Code](https://github.com/Perry961002/Learning-notes-of-SICP/tree/master/Chap1/exercise)  | [Code](https://github.com/Perry961002/Learning-notes-of-SICP/tree/master/Chap2/exercise) | --- | --- | --- |
