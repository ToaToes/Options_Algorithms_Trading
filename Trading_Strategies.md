期权量化主要有 4 大方向：
```
类型	                      核心思想	                  难度
波动率交易	                买卖 IV/RV 差	            高
Delta Neutral	            做 gamma/theta	          高
Directional	              用期权表达看涨跌	            中
Statistical Arbitrage	    skew / term structure	    很高
```

## 处理数据：
```
strike（行权价）
expiry（到期日）
IV（隐含波动率）
Greeks: (Black-Scholes)
    Delta（）
    Gamma（Delta 变化速率）
    Theta（时间流逝造成的损耗）
    Vega（IV变化率）
bid/ask（愿意买卖价格）
open interest（OI当前未平仓合约）
volume（成交量）
```
### Strike
```
Call：
Strike 越低 → 越贵
Strike 越高 → 越便宜
Put：
Strike 越高 → 越贵
Strike 越低 → 越便宜
```
### Expiry
```
时间越长：
期权通常越贵
因为有更多时间让价格波动
临近到期：
Theta decay（时间损耗）加速
OTM 期权可能快速归零
```
### IV
```
市场预期未来会波动多大。
    IV 高意味着
    市场认为：
    未来可能大涨大跌
    风险高
    不确定性高
    例如：
    财报前
    CPI
    黑天鹅
波动越大，
期权赚钱概率越高。
    IV Crush（非常重要）
    财报后经常发生：
    事件结束：
    不确定性消失
    IV 暴跌
    即使方向对：
    期权也可能亏钱
```
### Greeks
期权价格对各种因素变化的敏感度。<br>
**Delta**: <br>
    标的价格变化 $1，<br>
    期权价格变化多少。<br>
概率含义:<br>
    ATM：<br>
    delta ≈ 0.5<br>
    通常可粗略理解：<br>
    到期 ITM 概率约 50%<br>

**Gamma**:<br>
    股票动一点，<br>
    Delta 会变多少。<br>
```
Gamma 高的影响
近到期 ATM：
Gamma 最大。
意味着：
    盈亏变化极快
    可能瞬间从亏损变盈利
做市商 Gamma Hedging
Gamma 会影响：
    market maker 对冲
    squeeze
    pinning
这也是：
    “Gamma squeeze”来源。
```
**Vega**<br>
```
代表：<br>
    IV 变化 1%，<br>
    期权价格变化多少。<br>
Vega 高<br>
    意味着：<br>
    期权对 IV 非常敏感。<br>
Vega 最大<br>
    通常：<br>
    长期期权<br>
    ATM<br>
```  
财报交易核心<br>
```
财报前：
    Vega 风险极大
    IV inflate
财报后：
    Vega collapse
    IV crush
```






------------------------------------------------

### 项目1：Greeks Calculator
```
输入：
S, K, T, IV
输出：
delta gamma theta vega
```
### 项目2：Option Screener
```
扫描：
IV percentile
high skew
earnings IV spike
```
### 项目3：Wheel Strategy Backtest
```
这是最适合练习的。
涉及：
option chain
assignment
pnl
theta decay
但不会复杂到爆炸。
```
