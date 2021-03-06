## 记忆时间

## 卡片

### 0101. 反常识卡——

这本书的主题核心，就是最大的反常识卡，并且注意时间脉络。

### 0201. 术语卡——

根据反常识，再补充三个证据——就产生三张术语卡。

### 0202. 术语卡——

### 0203. 术语卡——

### 0301. 人名卡——

根据这些证据和案例，找出源头和提出术语的人是谁——产生一张人名卡，并且分析他为什么牛，有哪些作品，生平经历是什么。

### 0401. 金句卡——

最后根据他写的非常震撼的话语——产生一张金句卡。

### 0501. 任意卡——

最后还有一张任意卡，记录个人阅读感想。

## 书评

### 01

Martin Fowler 的《重构》，严格说来，我并没有完整的读完这本书，不过，正如作者自己所说，这样的书原本就不指望能够读完，因为有一大部分其实是参考手册。正是我读过的部分让我知道了重构，让我知道这么做可以把代码写得更好。Robert Martin 的《敏捷软件开发》，这是一本名字赶潮流，内容很丰富的书，这本书让我开始理解软件设计，从此不再刻意追求设计模式。Kent Beck 的《测试驱动开发》，我读的是英文版，因为当时中文版还没有出版，所以，我不敢说，我通过这本书很好的理解了测试驱动开发，但它却为我打开了一扇门，让我知道了一种更好的工作方式。

对于很多软件开发人员来说，加入一个公司，通常意味要面对一大堆之前留下的代码。而面对沉重的负担，大多数人的感觉都是无可奈何。让无奈成为往事，也就是这本书的价值所在。在我看来，这是一本讲解如何编写测试的书。之所以遗留代码让人头痛，除了复杂的逻辑，改动会带来怎样的后果是一件让人心里没底的事，而测试的存在可以大幅度降低这种恐惧。但是，许多代码在开发时并不考虑测试，这样做的结果就是让测试几乎成为一件不可能完成的任务，一个常见的例子就是代码中访问数据库。即便写出测试代码，漫长的测试过程也会让它失去一部分应有的作用，我们希望得到的是快速的反馈。所以，对于无测试而言，知道编写测试是一种境界的提升，写好单元测试则是一种更高的境界。如果能够让测试驱动开发，从开发之初便考虑测试，并懂得如何写好测试，开发者应该不会陷自己于一种难为的境地，这也应该成为专业程序员应该具备的基本技能。

至于这本书的具体内容，我的评价是实用。具体的手法，很难在这里一一列举，但是，以我的开发经验来看，许多似曾相识的代码不断的出现在书中，而作者举重若轻的处理手法，正是让我有拍案惊奇的地方。实际上，回味起来，每个手法都不是什么很高超的技法，但正是因为见识过类似的代码，才能体会到这种手法的价值所在。所以，相对于程序新人，它更适合有经验的人。之所以说这本书更适合有经验的人还因为，这本书中谈及的内容涵盖设计、测试、重构等诸多方面：通过重构，解开代码内的耦合，让其可测。这恰恰是前面提到的那三本书所讲的内容。也只有懂得了这些基本内容才能体会到那些具体手法的价值所在。依然记得当年读《重构》时，在提取和内联之间迷茫了好久，直到后来经过了许多开发实践才体会到这些做法的真正含义。

### 02

我现在就碰到了书中列出的种种问题：对已有的没有完善的单元测试的核心系统进行重构。为了保证少出乱子，不出乱子，我必须小心的对超大类，巨型方法采用各种重构手段进行修改，没有单元测试作保证的系统进行重构是非常危险的事儿，那怎么办呢，这本书让我知道了不少好的方法。与「重构到模式」一样，这也是一本围绕重构来阐述如何修改代码，只不过它面对的场景是遗留系统。对遗留系统进行重构首先要做的就是要让我们的修改能够被单元测试工具夹住，就像对一栋居民楼进行改造一样，必须先安装脚手架，拉上防护网，做好安全措施，然后再开工。从而减少因为修改带来的风险。

如何在修改代码前搞定对应的单元测试呢？这是一个非常有技巧的活儿，因为遗留系统可能因为设计不佳而无法或者很难非常容易的为其修改部分添加单元测试。之所以造成这样的局面一个重要的方面是无法对要测试的部分进行解除依赖。因此解除相关依赖也就成了修改代码首先面对的一个难题，本书在解除依赖方面总结了非常多的方法（或模式），这些方法总有一款会适合你。本人觉得这应该算是这本书的所要告诉我们的主要内容吧。

本书的例子大部分都是以 java 为主，少量的穿插了 c++ 的实例，而且有些手法跟语言的关系比较大，可能适用 c++ 的做法，对 java 并不适用。另外本书给我的另一个启发就是，我们在写代码的时候，应该尽量做好单元测试，单元测试可能在最初实现的时候，作用相对来说比较小，但是在后期维护修改重构以及添加新功能的时候，其威力将逐渐显现出来。此外一些系统之所以不好修改，后期维护困难，与我们编码时候没有遵循一定的规则有关，比如依赖管理，代码复杂度控制，这些规则其实都非常简单，人人都会知道，但是在具体场景能不能想到，并加以灵活运用却是另外一回事儿，我觉得这个必须经过大量的编码实践才能找到这种感觉，就像学习英语，只有多读，多听，多说，才能具有一定的语感，从而最终掌握。

### 04

若要体会好此书，个人建议按照步骤来读。步骤如下：1）确定改动点：画草图、影响结构图。2）找到测试点 ：在影响结构图根部。3）解依赖：重头戏，在第 25 章详细介绍了各种解依赖技术。4）编写测试：TDD。5）修改、重构：特征图。看完这些看完之后，胸中有了蓝图，心里面存在疑问了，咋解决大类，巨型方法啥的。如何动手处理呢。作者也专门弄了一章来如何在优化需求的情况下，如何一步一步的修改代码。

### 07

如果你想重构，重要的前提就是有强力的测试。哪怕你有自动化重构工具在手。如果你想对既有代码进行测试，你就必须先重构，因为代码根本就没有办法在测试工具中实例化。新写的代码大多是可以先进行测试，然后再挂接到原有代码中。而对付遗留的代码，我们则需要一点点地把代码抠出来测试。修改遗留代码时，我们需要将代码解依赖出来，建立其测试，然后才对它进行修改。并不是所有的重构手法都需要测试，特别是我们已经有了自动化的重构工具。书中说的一些解依赖技术就是一些特殊的重构技术。只要我们小步地前进，细心地操作，并借且自动化重构工具，无须测试就能进行重构。而这些重构技术的目标就是为重构出来的代码建立测试。一旦测试建立，则可对代码进行更为自信的修改，则可对代码进行更自信的进一步重构。

### 08

这本书讲解如何在不漂亮的旧代码下写漂亮的新代码，依照先有测试后有功能的思想，作者全书都围绕如何让代码可测试展开。如果旧代码特差，而又时间紧迫，不足以把旧代码纳入测试，通常是让新代码跟旧代码独立开。这可能需要用上继承，会让代码有不必要的层次，这没关系，重构一直在进行，只要代码纳入了测试，以后就可以把它们去掉。让代码纳入测试，很多时候是说能够用伪造的东西替换真实的东西，这个伪造的东西是测试用的。可以有很多种修改方法让代码能有单元测试，主要有几类方法：预处理期、链接期、修改代码（对象、方法的替换）。

本书看完之后，能回忆起来的东西很少，可能是因为没细看，也可能是写的太细了，实际工作中从来没有试过像书中所说的那样去写代码，步骤那么细，有必要吗？修改代码时，步伐要小是正确的，但小的书中所讲解的那种地步就有点受不了。本书可以总结为三个字「解依赖」，细节上就是各种各样的案例。

看这本书需要有大工程代码的修改经历，不然会觉得很无趣，我现在就有点无趣，跟第一次看设计模式一样的感觉。测试驱动开发，这是我初次接触到的概念，虽然工作中挂着敏捷的羊头，但我们的代码不存在单元测试，连影子也没有。看书的时候想，实际工作不一定要有真实的测试先行，只要头脑里有单元测试的思想，写代码的时候就会尽可能的往那一个方向去，在设计的时候就会想，假如需要测试代码能这样写吗？自然的就会让代码有更少的依赖，更多的分层，这也就有了单元测试的影子，依赖少了，可扩展也强了。这也就是读这本书的潜移默化的影响。

书里讲解看旧代码时，也讲解了些外围的东西，画图看代码就是很不错的方法。还有编译依赖导致一个工程的构建花费很多时间，这点书里谈到的不多，但工作中深感触，不必要的头文件包含、模板的滥用都会导致依赖增多，编译时间变长。这书跟《重构改善既有代码的设计》是同种类型。不过这本书怎么是这个书名呢？英文版是「Working Effectively with legacy Code」，也就是「在遗留代码上有效的工作」，强调的重点就不一样了。

看这本书有些名词不熟悉的压力，看到了很多新名词，譬如「函数签名」（其实就是形参），「朴素化参数」（可能是说让被切入测试的函数的参数是一般类型），「自由函数」（术语表有解释，C++ 中是非成员函数），「领域类」（就是 MVC 中的逻辑 M，这个词在《重构》上出现过）…… 这些新名词也不知道是不是通用的，如果不是通用的，搞出一个离本意遥远的新词来，又不在章节的开头给概述性解释，就真是让看者莫名其妙了（我又想到了那个「名字粉碎」的翻译，这本书里也用了它，很文艺很奇怪）。译者有些地方太小心了，加了不必要的译注，有些地方又感觉翻译得不容易快看，如果能意译会好些。

### 11

我的「重构三部曲」之三，（另外两本是《重构》，《从重构到模式》，这三本书让我对代码的理解有重生之感。大部分书都是教你怎么从 0 开始写好代码，但是现实是经常从接手已有的项目开始，所以这三本就很有价值。这本书压箱底 8，9 年了，前些年有次囫囵吞枣看到 100 多页就放弃了，因为看不懂。有了前两本垫底，这次阅读就轻松多了。书给我最大的震撼是在开头，「遗留代码」legacy code 的定义！一般我们会把别人写的代码定义为遗留代码，或者自己的代码写着写着就变成了遗留代码。书中对遗留代码的定义非常明确：「遗留代码就是那些没有编写相应测试的代码。」由此凸显测试驱动开发的重要性，简单说我觉得有 3 点，1）测试是一种即时反馈的技术，能帮助尽早快速定位到 bug。2）从可测试的角度能够写出更好的代码，因为会关注依赖，测试的过程本身也是对代码理解的过程。3）「通过单元测试」是代码质量一个可测量的指标。是设计不足与过度设计的分界点。（好吧，这点我说的有点虚，希望一年内，我能整理出在 iOS 上测试的流程、工作和经验。）

这本书分为三部分：1）修改机理，讲作者修改代码的方法论。2）修改代码的技术，将代码中遇到的坑一个个罗列出来，而且给出非常实用的对付手段，绝不理论和太极。3）借依赖技术。不合理的依赖是万恶之源，这章有 24 小结专门介绍怎么对付他们。话说，看完之后，我忘了大半，等我 TDD 做起来之后再来验证性的看一遍。