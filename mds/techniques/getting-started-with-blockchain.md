#  区块链入门

作者: [songtianyi](https://github.com/songtianyi) 2018-08-19

### 前言

比特币作为近两年来的大热潮，其价格能在2个月的时间从5000美元增长到1500美元，一年增长近10倍，疯狂程度令人咂舌。资本或者说人都是逐利的，这股浪潮催生了大量的创业公司和相对较高薪水的技术岗位，不管你是否准备从事此行业，了解其背后的技术都是必要的，至少不至于被别人的思想所左右。区块链火了这么久，不管是文章还是书籍都多如牛毛，为什么还会有这篇文章呢？权当是自己学习区块链过程中的一个笔记吧。

### 背景

公认的最早关于区块链的描述性文献是中本聪所撰写的 《比特币：一种点对点的电子现金系统》，根据此论文实现的比特币网络在无集中式管理的情况下， 稳定运行了近十年时间，支持了海量的交易记录，并未出现严重的漏洞。比特币历史上唯一已知的漏洞事件曾导致比特币的恶意增发，但问题很快被发现并修正，相关非法交易被撤销。关于比特币更详细的历史，可以查看[wikipedia](https://zh.wikipedia.org/wiki/%E6%AF%94%E7%89%B9%E5%B9%A3%E6%AD%B7%E5%8F%B2)。在中本聪的论文中，区块链被描述为用于记录比特币交易的账目历史。区块链技术成型于比特币，作为比特币背后的分布式记账平台，其解决了哪些问题？

### 从货币说起

中国的货币发展史

- 贝壳，是中原一带最早的货币形式，是一种主导位置的货币，汉字中很多交换有关的字都是以贝作为部首的，比如 "赚",“货” 等。起初，人们都是以物易物来进行价值交换，其弊端很明显，比如张三手里有一只兔子，想用来换李四的一只鸭，但李四并不想要兔子，他想要小花儿的鹅，以此类推，将所有人的需求聚集起来以物易物是不现实的，而通过贝壳这种一般等价物可以实现任意两人之间的价值交换。
- 铜币，因为贝壳的总量是极其丰富的，每个人都可以生产货币导致没人去创造真正的价值，商朝的时候出现了铜币，铜币的稀缺性很好地解决了这个问题，而且其性状稳定，便于携带，是比较完美的一般等价物。
- 铜钱, 铜币属于民间货币，大小不一，纯度不一，在交换的时候很容易产生争执，后来秦始皇统一度量，统一货币，使用铜钱。
- 交子，随着经济的发展，人们在购买高价值的商品或服务时，交付大量的货币可能需要跋山涉水，还要担心被抢走，在宋代，纸币(交子，是人类历史上最早的纸币)出现了，商人们联合发行一种记账票据，实现金属货币的异地交付，降低交易成本。
- 金银，元明两代纸币出现了严重的通货膨胀，为什么呢？商人逐利，本来大家往他那儿存了100两的货币，他却放出了1000两的票据，反正一时半会儿不会有人来兑，这样市面流通的票据越来越多，就形成了通胀。怎么办呢？国家收回了纸币的发行权，并和金银这种极稀缺的金属挂钩，即金本位。
- 布雷顿森林体系，一战和二战期间，各国都需要大量的钱来打仗，于是发行了大量的不可兑换(和上述的奸商一样)的纸币, 最终国家破产。二战结束时，美国主导制定了《布雷顿森林协定》，此协定是各国就货币的兑换、国际收支的调节、国际储备资产的构成等问题共同作出的安排所确定的规则、采取之措施及相应组织机构形式的总和。布雷顿森林体系是以锚定黄金的美元作为国际流通货币。1960～70年代爆发多次美元危机，1971年12月在尼克森时代，美国美联储拒绝向国外中央银行出售黄金，至此美元与黄金挂钩的体制名存实亡；1973年2月美元进一步贬值，世界各主要货币受投机客打击被迫实行[浮动汇率](https://zh.wikipedia.org/wiki/%E6%B5%AE%E5%8B%95%E5%8C%AF%E7%8E%87)制，至此布雷顿森林体系完全崩溃。全球主要货币进入全面自由浮动的时代，亦称为“后布雷顿森林时代。
- 从布雷顿森林体系结束之后，人类进入信用货币的时代，就是以政府信用为背书，通过立法来发行货币。随着移动互联网的发展，我们已经在逐渐脱离实物货币，使用数字货币，比如微信，支付宝，信用卡等，但本质上还是信用货币。
- 信用的货币的优点是可以超发，以刺激经济的发展，其缺点也是可以超发，因为你发多了，就相当于无形地掠夺了大众的财富。信用货币属于中心化的货币，国家想发多少发多少，而比特币则提供了新的思路，即去中心化，试图摆脱政府对货币发行的控制。其总量固定，不会出现通胀，而且不受任何单一组织的控制。但在国内，比特币不是合法货币，交易渠道也被陆续封锁。

### 去中心化

在比特币出现之前，人们一直在尝试用互联网技术解决现行货币体系的通胀和低效问题。1998年，Nick Szabo提出了一种去中心化的数字货币Bit-Gold，但并未被实现。Bit-Gold和Bitcoin有很多相似的地方，比如POW等，Bit-gold被认为是Bitcoin的前身。为什么要去中心化？

中心化的缺点:

如何去中心化

p2p



### 记账

区块

发币

交易

### 智能合约

### 演进路线

### 参考资料

* 《精通比特币》
* ​



