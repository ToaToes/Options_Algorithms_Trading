期权量化主要有 4 大方向：
```
类型	                      核心思想	                  难度
波动率交易	                买卖 IV/RV 差	            高
Delta Neutral	            做 gamma/theta	          高
Directional	              用期权表达看涨跌	            中
Statistical Arbitrage	    skew / term structure	    很高
```

处理数据：
```
strike
expiry
IV
Greeks: (Black-Scholes)
    Delta
    Gamma
    Theta
    Vega
bid/ask
open interest
volume
```

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
