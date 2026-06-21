# Advanced Financial Market & Investment Analyzer
[![Inserloft](https://img.shields.io/badge/Inserloft-Advanced%20Skills-purple)](https://inserloft.com/skills)
[![License](https://img.shields.io/badge/License-Proprietary-blue)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0-green)](CHANGELOG.md)
[![AI Powered](https://img.shields.io/badge/AI%20Powered-Cleo-purple)](https://inserloft.com)
## Overview

The **Advanced Financial Market & Investment Analyzer** is a production-grade AI skill for expert-level stock market analysis, technical pattern recognition, portfolio risk management, and data-driven investment predictions. This skill empowers Claude to function as a tier-1 financial analyst, providing institutional-quality analysis grounded in established financial frameworks and strict data integrity standards.

### Key Capabilities

- **Technical Pattern Recognition**: Japanese candlestick analysis with contextual interpretation (Doji, Hammer, Engulfing, Morning Star, etc.)
- **Fundamental Analysis**: Valuation metrics, profitability analysis, growth assessment, financial health evaluation
- **Momentum & Trend Analysis**: RSI, MACD, Moving Averages, Volume Profile with proper divergence detection
- **Portfolio Risk Management**: Position sizing (Kelly Criterion), correlation analysis, rebalancing protocols, risk metrics
- **Market Prediction Frameworks**: Multi-scenario forecasting (Base/Bull/Bear cases) with confidence grading and probability assessment
- **Data Integrity**: Strict prohibition on hallucinated data; requires explicit source attribution and uncertainty quantification

---

## When to Trigger This Skill

Consult this skill whenever the user:

- **Analyzes stock charts** or requests candlestick pattern identification
- **Asks about technical indicators** (RSI, MACD, moving averages, support/resistance)
- **Needs portfolio risk assessment** or rebalancing strategy
- **Requests market forecasts** or price predictions
- **Evaluates fundamentals** (P/E, revenue growth, debt ratios, valuation)
- **Seeks investment recommendations** with risk/reward analysis
- **Questions trend continuation/reversal** patterns
- **Needs position sizing guidance** or risk allocation frameworks
- **Analyzes sector rotation** or correlation between holdings

---

## Core Frameworks

### 1. Technical Analysis

The skill employs six primary frameworks:

**Candlestick Patterns**
- Single candles (Doji, Hammer, Shooting Star, Marubozu)
- Multi-candle patterns (Engulfing, Harami, Morning Star, Evening Star, Three Soldiers/Crows)
- Pattern validity rules: Volume confirmation, trend context, timeframe hierarchy

**Momentum Indicators**
- RSI (Relative Strength Index): Overbought/oversold detection and divergence analysis
- MACD: Trend following with histogram and crossover confirmation
- Moving Averages: Golden Cross, trend structure, price relationship

**Volume Analysis**
- High-volume nodes as support/resistance
- Volume confirmation on pattern validation
- Divergence detection (volume decline on price move)

**Support & Resistance**
- Horizontal zones from prior peaks/troughs
- Fibonacci levels for price projections
- Trendline breaks as invalidation signals

### 2. Fundamental Analysis

Integrated valuation and business quality assessment:

**Valuation Metrics**
- P/E Ratio (vs. historical and sector peer comparison)
- Price-to-Book, PEG Ratio, EV/EBITDA
- Intrinsic value frameworks

**Profitability & Returns**
- Net Margin, ROE, ROA trending
- Quality of earnings assessment

**Growth Metrics**
- Revenue and EPS growth rates (YoY)
- Free cash flow growth (most reliable)

**Financial Health**
- Debt-to-Equity, Current Ratio, Interest Coverage
- Liquidity assessment

### 3. Risk Management

**Position Sizing**
- Modified Kelly Criterion for realistic position allocation
- Per-trade risk caps (1-3% of portfolio)
- Sector concentration limits and beta balancing

**Portfolio Optimization**
- Correlation analysis (target 0.3-0.5 portfolio correlation)
- Quarterly rebalancing threshold (5% drift trigger)
- Tax-aware rebalancing for taxable accounts

**Risk Metrics**
- Volatility (Standard Deviation)
- Sharpe Ratio (risk-adjusted returns)
- Maximum Drawdown
- Value at Risk (VaR)

### 4. Prediction Framework

**Multi-Scenario Forecasting**

Predictions must include three scenarios:

1. **Base Case** (50% probability): Primary thesis with price target and timeframe
2. **Bull Case** (25% probability): Upside catalyst and target
3. **Bear Case** (25% probability): Primary risk and downside scenario

**Confidence Grading**
- High Confidence (70-85%): Clear pattern + fundamental alignment + volume confirmation
- Medium Confidence (55-70%): Pattern valid, mixed signals or limited precedent
- Low Confidence (40-55%): Early setup; monitor for confirmation

---

## Data Requirements

For any analysis, the skill requires:

1. **Price Data**: OHLC (Open, High, Low, Close) + Volume
2. **Timeframe Specification**: Daily, weekly, 4-hour, intraday, etc.
3. **Chart Context**: Current level, recent highs/lows, support/resistance zones
4. **Fundamental Data** (if applicable): Latest earnings, revenue, P/E, debt levels
5. **Comparative Context**: Sector and S&P 500 performance reference

### Data Validation

All analysis includes verification:
- Sufficient historical candles (minimum 20+) for pattern analysis
- Volume data logical correlation with price
- No data gaps or anomalies
- Currency specification for non-US equities
- Adjustment for splits/dividends on historical comparisons

---

## Non-Negotiable Rules

1. **No Hallucinated Data**: All price points, returns, or metrics must cite sources
2. **Probabilistic Thinking**: Predictions framed as confidence intervals, not certainties
3. **Risk-First Mindset**: Downside assessment before upside potential
4. **Framework Transparency**: State analytical method and its limitations
5. **Source Attribution**: Reference data origins (user chart, terminal, academic study, etc.)

---

## Output Standards

Every analysis includes:

| Component | Content |
|-----------|---------|
| **Executive Summary** | Thesis and primary recommendation (2-3 sentences) |
| **Technical Analysis** | Patterns, indicators, key levels with volume confirmation |
| **Fundamental Analysis** | Valuation, growth, financial health (if available) |
| **Risk Assessment** | Downside scenarios, stop-loss levels, position sizing |
| **Action Plan** | Entry points, profit targets, monitoring criteria |

---

## Limitations & Escalation

### When Analysis is Unavailable

- **Real-time data gaps**: Explicitly state data cutoff date
- **Insufficient data**: Request missing metrics or recommend data sources
- **Complex derivatives**: Options/futures → basic framework only; recommend specialist
- **Regulatory concerns**: Tax optimization, insider trading → defer to compliance

### Uncertainty Communication

When confidence is below 70%:
- Explicitly state confidence level (High/Medium/Low)
- Recommend paper trading or small position sizing
- Provide specific signals that would increase confidence
- Frame as "Monitor for confirmation before scaling"

---

## Example Use Cases

### Use Case 1: Japanese Candlestick Analysis

**Input**: Daily chart of MSFT showing a three-candle pattern

**Expected Output**:
- Pattern identification with probability assessment
- Volume profile confirmation
- Support/resistance context
- Risk/reward ratio for hypothetical position
- Confidence level and monitoring criteria

### Use Case 2: Portfolio Risk Assessment

**Input**: List of 10 holdings with allocation percentages and correlations

**Expected Output**:
- Concentration risk analysis
- Optimal rebalancing targets
- Tax impact assessment
- Volatility and Sharpe Ratio projections
- Recommended adjustment timeline

### Use Case 3: Market Prediction

**Input**: Technical + fundamental data on a stock showing mixed signals

**Expected Output**:
- Base/Bull/Bear case scenarios with probabilities
- Price targets with timeframes for each scenario
- Invalidation signals for each thesis
- Confidence grading with supporting evidence
- Specific entry/exit points with risk levels

---

## Technical References

### Candlestick Pattern Validity

Patterns require different confirmations based on context:

| Pattern Type | Context | Confirmation |
|-------------|---------|--------------|
| Reversal | At support/resistance | Volume spike + follow-through candle |
| Reversal | In mid-trend | Higher timeframe confirmation needed |
| Continuation | In trend | Volume sustain + price continuation |
| Indecision (Doji) | Any zone | Requires follow-up candle for direction |

### Indicator Interpretation Guidelines

**RSI in Trending Markets**
- Uptrend: RSI often stays 60-85 (not a sell signal)
- Downtrend: RSI often stays 15-40 (not a buy signal)
- Divergence: Price new high, RSI fails to confirm → potential exhaustion

**Moving Averages**
- Price > 50-day > 200-day: Bullish alignment
- Price < 50-day < 200-day: Bearish alignment
- Crossovers: Crossovers are lagging; combine with price action

**Volume Profile**
- High volume at price level: Strong support/resistance
- Volume surge on breakout: Confirms directional move
- Declining volume on move: Warns of weakening momentum

---

## Risk Disclaimers

This skill provides **analytical frameworks and probability-based insights**, not financial advice. 

**Important Limitations**:
- Past performance does not guarantee future results
- Technical patterns have variable predictive power depending on context
- Fundamental metrics depend on data quality and accounting standards
- Market predictions always carry uncertainty; use conservative position sizing
- Tax and regulatory implications vary by jurisdiction

---

## Integration with Other Tools

This skill complements:

- **Real-time market data feeds**: For current prices and charts
- **Financial terminals**: Bloomberg, FactSet, E*TRADE for institutional data
- **Risk management systems**: Portfolio allocation and rebalancing software
- **Backtesting platforms**: Validate pattern analysis on historical data

---

## Revision History

- **v1.0** (2026-06-20): Initial release with Japanese candlestick patterns, fundamental analysis, risk management, and prediction frameworks

---

## Watermark

Inserloft
web: wwww.Inserloft.com
Skill web: wwww.Inserloft.com/Skills/advanced-finance-analyzer
