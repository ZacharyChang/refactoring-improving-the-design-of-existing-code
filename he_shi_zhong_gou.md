# 何时重构

几乎任何情况下我都反对专门拨出时间进行重构。在我肴来，重构本来就不是一件应该特别拨出时间做的事情，重构应该随时随地进行。你不应该为重构而重构,你之所以重构，是因为你想做别的什么事，而重构可以帮助你把那些事做好。

## 三次法则

DonRoberts给了我一条准则：第一次做某件事时只管去做；第二次做类似的事会产生反感，但无论如何还是可以去做；第三次再做类似的事，你就应该重构。

**事不过三，三则重构。**

## 添加功能时重构

最常见的重构时机就是我想给软件添加新特性的时候。此时，重构的直接原因 往往是为了帮助我理解需要修改的代码。

在这里，重构的另一个原动力是：代码的设计无法帮助我轻松添加我所需要的特性。之所以这么做，部分原因是为了让未来增加新特性时能够更轻松一些，但最主要的原因还是：我发现这是最快捷的途径。重构是一个快速流畅的过程，一旦完成重构，新特性的添加就会更快速、更流畅。

## 修补错误时重构

调试过程中运用重构，多半是为了让代码更具可读性。当我看着代码丼努力理解它的时候，我用重构帮助加深自己的理解。我发现以这种程序来处理代码，常常能够帮助我找出bug。你可以这么想：如果收到一份错误报告，这就是需要重构的信号，因为显 然代码还不够清晰——没有清晰到让你能一眼看出bug。

## 复审代码时重构

我发现，重构可以帮助我复审别人的代码。开始重构前我可以先阅读代码，得到一定程度的理解，并提出一些建议。

重构还可以帮助代码复审工作得到更具体的结果。不仅获得建议，而且其中许多建议能够立刻实现。最终你将从实践中得到比以往多得多的成就感。

为了让过程正常运转，你的复审团队必须保持精练。就我的经验，最好是一个复审者搭配-个原作者，共同处理这些代码。复审者提出修改建议，然后两人共同判断这些修改是否能够通过重构轻松实现。果真能够如此，就一起着手修改。

如果是比较大的设计复审工作，那么在一个较大团队内保留多种观点通常会更好一些。此时直接展示代码往往不是最佳办法。我喜欢运用UML示意图展现设计，并以CRC卡展示软件情节。换句话说，我会和某个团队进行设计复审，而和单个复审者进行代码复审。

极限编程[Beck, XP] 中的“**结对编程**”形式，把代码复审的积极性发挥到了极致。一旦采用这种形式，所有正式开发任务都由两名开发者在同一台机器上进行。这样便在开发过程中形成随时进行的代码复审工作，而重构也就被包含在开发过程内了。

# 为什么重构有用？  ——Kent Beck

是什么让程序如此难以相与？眼下我能想起下述四个原因，它们是：
* 难以阅读的程序，难以修改；
* 逻辑重复的程序，难以修改；
* 添加新行为时需要修改已有代码的程序，难以修改； 
* 带复杂条件逻辑的程序，难以修改。

因此，我们希望程序：
1. 容易阅读；
2. 所有逻辑都只在唯一地点指定；
3. 新的改动不会危及现有行为；
4. 尽可能简单表达条件逻辑。

重构是这样一个过程：它在一个目前可运行的程序上进行，在不改变程序行为的前提下使其具备上述美好性质，使我们能够继续保持高速开发，从而增加程序的价值。