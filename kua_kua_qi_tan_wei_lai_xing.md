# 夸夸其谈未来性 Speculative Generality

这个令我们十分敏感的坏味道，命名者是Brian Foote。当有人说“噢，我想我们总有一天需要做这事”，并因而企图以各式各样的钩子和特殊情况来处理一些非必要的事情，这种坏味道就出现了。那么做的结果往往造成系统更难理解和维护。如果所有装置都会被用到，那就值得那么做：如果用不到，就不值得。用不上的装置只会挡你的路，所以，把它搬开吧。

如果你的某个抽象类其实没有太大作用，请运用Collapse Hierarchy 。不必要的委托可运用Inline Class除掉。如果函数的某些参数未被用上，可对它实施 Remove Parameter。如果函数名称带有多余的抽象意味，应该对它实施Rename Method,让它现实一些。

如果函数或类的唯一用户是测试用例，这就飘出了坏味道Speculative Generality。如果你发现这样的函数或类，请把它们连同其测试用例一并删掉。但如果它们的用途是帮助测试用例检测正当功能，当然必须刀下留人。 