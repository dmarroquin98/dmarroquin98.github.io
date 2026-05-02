# 📈 Multi-Asset Portfolio Construction & Optimization
### Quantitative Portfolio Management — Group Assignment

> **Course Project** · Portfolio Management · Daniel Marroquín  
> Tools: Microsoft Excel · Mean-Variance Optimization · Sharpe Ratio Maximization

---

## 📌 Overview

Construction and performance evaluation of an **Optimal Risky Portfolio** across four asset classes using real market data. The portfolio was built following a structured Investment Policy Statement (IPS), optimized via Mean-Variance analysis, and benchmarked against market indices.

---

## 🗂️ Asset Universe — 9 ETFs across 4 Asset Classes

| # | Ticker | Security Name | Asset Class | Rationale |
|---|---|---|---|---|
| 1 | **GLD** | SPDR Gold Shares | Commodity | Defensive hedge; strong during recessions |
| 2 | **WCOA.MI** | WisdomTree Enhanced Commodity UCITS ETF | Commodity | Diversified exposure to energy, metals & agriculture |
| 3 | **COFF.L** | WisdomTree Coffee | Commodity | Speculative upside — drought impact in Latin America |
| 4 | **XIU.TO** | iShares S&P/TSX 60 Index ETF | Equity | Broad Canadian market exposure, dividend income |
| 5 | **SPY** | SPDR S&P 500 ETF Trust | Equity | U.S. large-cap growth; tech & healthcare exposure |
| 6 | **AGG** | iShares Core U.S. Aggregate Bond ETF | Bond | U.S. investment-grade bond market |
| 7 | **ZRR.TO** | BMO Real Return Bond Index | Bond | Canadian inflation-linked bonds |
| 8 | **VAB.TO** | Vanguard Canadian Aggregate Bond Index | Bond | Diversified Canadian fixed income |
| 9 | **VRE.TO** | Vanguard FTSE Canadian Capped REIT Index ETF | Real Estate | Canadian REIT sector exposure |

---

## ⚙️ Methodology

### 1. Data Collection
- Monthly price data for all 9 ETFs
- **n = 78 monthly observations**
- Returns computed as Holding Period Yield (HPY)
- Risk-free rate sourced monthly for excess return calculations

### 2. Statistical Analysis
- Mean return and risk premium per asset
- Standard deviation (risk) per asset
- **Full 9×9 covariance matrix** (population and sample-adjusted)
- **Correlation matrix** to assess diversification benefits

### 3. Portfolio Optimization
- **Objective**: Maximize Sharpe Ratio (Optimal Risky Portfolio)
- **Constraint**: Weights sum to 1 (long-only)
- Solved via Excel Solver using mean-variance framework
- Benchmark: Composite index (BCOM + S&P/TSX Composite)

### 4. Performance Evaluation
Four risk-adjusted performance measures were computed and compared against the benchmark:

| Measure | Formula | What it captures |
|---|---|---|
| **Treynor** | (Rp - Rf) / β | Return per unit of systematic risk |
| **Sharpe** | (Rp - Rf) / σp | Return per unit of total risk |
| **Jensen's Alpha** | Rp - [Rf + β(Rm - Rf)] | Excess return over CAPM prediction |
| **Information Ratio** | (Rp - Rm) / Tracking Error | Active return per unit of active risk |

---

## 📊 Optimal Portfolio — Results

### Capital Allocation (Optimal Risky Portfolio)

| Ticker | Asset Class | Weight |
|---|---|---|
| **GLD** | Commodity | **31.73%** |
| **WCOA.MI** | Commodity | **18.96%** |
| **COFF.L** | Commodity | **11.94%** |
| **XIU.TO** | Equity | 0.22% |
| **SPY** | Equity | **37.14%** |
| AGG | Bond | 0% |
| ZRR.TO | Bond | 0% |
| VAB.TO | Bond | 0% |
| VRE.TO | Real Estate | 0% |

> The optimizer heavily allocated to commodities (GLD, WCOA.MI, COFF.L) and U.S. equities (SPY), reflecting their superior risk-adjusted return profile during the sample period.

### Portfolio Statistics (Monthly)

| Metric | Value |
|---|---|
| Mean Return | 0.993% |
| Mean Risk Premium | 0.815% |
| Standard Deviation | 2.62% |
| **Annualized Return** | **12.59%** |
| **Annualized Risk Premium** | **10.23%** |
| **Annualized Std. Dev.** | **9.07%** |
| **Sharpe Ratio** | **0.3188** |
| Beta (vs benchmark) | 0.4238 |

### Performance vs Benchmark

| Measure | Benchmark | Portfolio | Result |
|---|---|---|---|
| Treynor | -0.00135 | **0.01923** | ✅ Portfolio wins |
| Sharpe | -0.0545 | **0.3111** | ✅ Portfolio wins |
| Information Ratio | — | **0.3411** | ✅ Positive active return |
| Jensen's Alpha | 0 | **+0.00872** | ✅ Portfolio wins |

> **The portfolio outperformed the benchmark across all four risk-adjusted performance measures.**

---

## 📐 Correlation Highlights

Key correlations from the 9×9 matrix:

- **XIU.TO ↔ SPY**: 0.803 — high positive (both equity, expected)
- **ZRR.TO ↔ VAB.TO**: 0.867 — high positive (both Canadian bonds)
- **GLD ↔ AGG**: 0.464 — moderate positive (flight-to-safety assets)
- **WCOA.MI ↔ VAB.TO**: -0.332 — negative (diversification benefit)
- **GLD ↔ VRE.TO**: 0.006 — near-zero (excellent diversifier)

---

## 📁 Repository Structure

```
portfolio-optimization/
├── README.md                                          ← This file
├── portfolio-dashboard.html                           ← Interactive dashboard
└── Group_Assignment-Marroquin-Phan-Fernando-Saini.xlsx ← Full Excel model
```

---

## 🛠️ Tools & Techniques

| Tool | Application |
|---|---|
| **Microsoft Excel** | Data collection, return calculation, covariance matrix, Solver optimization |
| **Excel Solver** | Mean-variance optimization to maximize Sharpe Ratio |
| **Statistical Methods** | HPY returns, covariance/correlation matrices, beta estimation |
| **Performance Analysis** | Treynor, Sharpe, Jensen's Alpha, Information Ratio, Tracking Error |

---

*Project by Daniel Marroquín · Vancouver, BC · Open to roles in Portfolio Management, Quantitative Finance, and Investment Analysis in Canada*
*[View interactive dashboard →](./portfolio-dashboard.html)*
