常见标的资产类型：
```
类型	例子
股票	苹果、腾讯
指数	标普500、恒生指数
商品	黄金、原油、玉米
利率	国债收益率、LIBOR
汇率	美元/人民币、欧元/美元
```

**Derivatives** 衍生品研究的是基于标的资产(**Underlying Assets**)或指数价值(**Index Value**)的金融合约，内容包括：
```
合约的特征和工具类型: features and instruments
收益、风险及用途: benefits, risks and uses
套利与持有成本: abitrage and cost of carry
远期、期货、互换和期权的定价与估值: forwards, futures, swaps and options, their pricing and valuation
利用看涨-看跌平价关系进行复制: replication using put-call parity
利用二叉树模型进行估值: valuation using binomial model
```

Abitrage: 套利，在同一时间、不同市场或不同合约之间，无风险地低买高卖，赚取价差。<br>
在期权中的经典例子（Put-Call Parity）：
```
如果看涨期权 + 现金 ≠ 看跌期权 + 股票
套利者会买入便宜的一方，卖出贵的一方，赚取差价
这个套利行为会把价格拉回合理水平，这就是你之前问的“为什么定价模型有效”的根本原因
```
基本上等同于同时买入低估期权 卖出高估期权，最后两笔交易独立清算与结算，获取差价<br>
差价是如何消失的：
Call + 现金 = 用固定资金锁定未来买入权<br>
Put + 股票 = 用股票锁定未来卖出权<br>

# _S + P - C = Pv（x）_ <br>
其中：<br>
**欧式期权：**看涨-看跌平价成立，是因为 payoff 只在到期 T 才实现，因此可以用贴现现金 + 股票 + 期权做静态复制；<br>
**美式期权：**由于允许提前行权，使 payoff 时间不固定，从而破坏严格平价关系。<br>
