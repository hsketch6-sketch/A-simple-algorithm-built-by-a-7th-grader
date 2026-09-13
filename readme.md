| Period        |    V4 CAGR | B&H CAGR |      Alpha |         MDD |    Sharpe | Trades | Win Rate | Interpretation                                             |
| ------------- | ---------: | -------: | ---------: | ----------: | --------: | -----: | -------: | ---------------------------------------------------------- |
| **2000–2005** |     -4.79% |   -1.62% |     -3.17% |     -57.65% |    -0.089 |      5 |     100% | 🔴 Extremely difficult semiconductor environment           |
| **2000–2015** |      5.13% |    2.31% | **+2.82%** |     -57.65% |     0.343 |     25 |     100% | 🟡 Weak long-term environment                              |
| **2010–2015** |      1.83% |    6.77% | **-4.94%** |     -41.36% |     0.193 |     15 |   93.33% | 🔴 One of the weakest periods                              |
| **2010–2020** |     17.63% |   17.20% | **+0.43%** |     -41.36% |     0.794 |     15 |   93.33% | 🟡 Roughly matched the benchmark                           |
| **2010–2026** |     22.92% |   20.39% | **+2.53%** |     -41.36% |     0.917 |     30 |   96.67% | 🟢 Positive long-term alpha                                |
| **2015–2026** | **33.75%** |   24.65% | **+9.10%** | **-32.05%** | **1.194** |     15 |     100% | 🟢🟢 Strongest major test                                  |
| **2020–2026** | **33.13%** |   26.18% | **+6.96%** |     -33.15% |     1.076 |     15 |     100% | 🟢🟢 Strong recent-cycle performance                       |
| **2025–2026** | **79.35%** |   99.47% |    -20.12% | **-14.05%** | **2.467** |      0 |      N/A | 🟢 Extreme bull market; B&H was exceptionally hard to beat |
What the results suggest

The pattern is quite clear:

2000–2015:
V4 was relatively weak. The semiconductor industry experienced major disruptions and did not consistently develop the kind of sustained cycle that V4 is designed to exploit.

2015–2026:
This is where V4 becomes much more compelling:

33.75% CAGR vs. 24.65% B&H
+9.10 percentage points of alpha
-32.05% MDD
1.194 Sharpe ratio

The strategy was able to outperform the benchmark while substantially controlling drawdowns.

2020–2026 gives a very similar result, which is particularly interesting because the strong performance is not isolated to one narrow period.

2025–2026 is a special case. B&H achieved an extraordinary 99.47% CAGR, so V4's -20.12% alpha does not necessarily indicate poor performance. V4 still produced 79.35% CAGR with only -14.05% MDD and a 2.467 Sharpe ratio.

2. What exactly is the V4 algorithm?

V4 is essentially a semiconductor cycle-following strategy.

The core idea is:

Don't try to predict which semiconductor stock will rise tomorrow. Instead, wait for the semiconductor industry to enter a favorable low-volatility phase, identify the strongest stocks relative to the semiconductor sector, and stay invested through the cycle until the cycle itself shows signs of ending.

It has four major components.

A. Detect a quiet semiconductor environment

V4 monitors the SOX Semiconductor Index.

It calculates volatility using ATR and looks for unusually quiet conditions.

The strategy requires both:

SOX volatility to be unusually low
Individual stock volatility to be unusually low

The threshold is approximately the lowest 10% of the historical volatility distribution.

The idea is that major semiconductor moves often don't begin while volatility is already extremely elevated.

B. Select the strongest semiconductor stocks

Once the volatility conditions are satisfied, V4 calculates relative strength against SOX.

It does not simply ask:

"Which stock went up the most?"

Instead:

"Which semiconductor stocks are outperforming the semiconductor sector?"

The top 5 relative-strength stocks are eligible for purchase.

This is important because the strategy isn't trying to own the entire semiconductor industry equally.

It wants to concentrate on the companies that are demonstrating leadership within the semiconductor cycle.

C. Stay invested during the cycle

This is one of the most important characteristics of V4.

V4 is not a short-term trading system.

Once a position is established, it can remain open for a very long time.

The backtests show average holding periods of roughly:

800–1,000+ trading days in several long periods
sometimes several years

This is intentional.

The philosophy is:

If the semiconductor cycle is working, don't keep selling just because the stock has already gone up a lot.

The strategy wants to capture the large middle portion of the cycle, rather than repeatedly trying to enter and exit small moves.

D. Detect the end of the semiconductor cycle

The full exit is based on the SOX cycle structure, rather than an individual stock's short-term movement.

Conceptually, V4 looks for:

A → B → C → breakdown

where:

A: major cycle high
B: meaningful pullback low
C: recovery/rebound after the pullback
B breakdown: the market subsequently falls back through the previous pullback low

That final breakdown is treated as evidence that the semiconductor cycle itself may be ending.

The positions are then exited on the next trading day's opening price.

3. Additional risk management

V4 also monitors the SOX 200-day moving average.

If:

SOX < 200-day MA

the strategy reduces each affected position by 50%.

If SOX subsequently recovers above the MA, the previously reduced shares are restored.

So the MA200 is not the main entry/exit system.

It is more like a temporary risk-reduction mechanism.

4. The philosophy in one sentence

If I had to describe V4 in one sentence:

V4 is a long-only semiconductor cycle strategy that waits for unusually low volatility, selects the strongest semiconductor stocks relative to SOX, holds them through the major upside phase of the cycle, and exits when the semiconductor sector itself shows structural evidence of cycle failure.

And that's also why the historical results make sense.

V4 isn't designed to outperform during every possible market regime.

It's designed to answer a much narrower question:

"When a real semiconductor cycle develops, can we systematically identify the leaders early enough and stay with them long enough to capture the cycle?"

Based on the current backtests, 2015–2026 and 2020–2026 provide the strongest evidence that the answer may be yes.

The weaker 2000–2015 results are important too, because they show that V4 does have a regime dependency rather than magically making money in every environment. That actually makes the backtest more informative, not less.
V4 has also demonstrated an important robustness characteristic: across the semiconductor tickers we tested, the strategy generally avoided the major “landmines” that severely damaged individual buy-and-hold investors.
(like CSCO, INTC, .... )
Benchmark Universe

The Buy & Hold (B&H) benchmark consisted of the following 13 tickers:

MU, NVDA, AMD, AMAT, LRCX, KLAC, QCOM, TXN, ADI, INTC, WDC, STX, CSCO

The B&H benchmark represents the performance of holding these stocks throughout the tested period, with the average CAGR calculated across valid tickers.
