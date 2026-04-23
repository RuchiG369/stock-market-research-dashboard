
# Methodology

## Objective

The purpose of this dashboard is to identify strong stocks and sectors during market hours using a structured ranking process.

The dashboard is designed to support a research analyst by reducing manual scanning and making the market easier to interpret in real time.

## Universe

The project focuses on Indian equities and uses a defined stock universe mapped to sectors.

The output is designed around:
- stock-level ranking
- sector-level strength
- trade-readiness
- decision-ready presentation

## Data Flow

The process works in the following sequence:

1. instrument mapping is prepared
2. live intraday market data is fetched
3. stock-level signals are calculated
4. sector-level strength is calculated
5. rankings are generated
6. results are saved to output files
7. dashboard reads the latest files and refreshes

## Stock-Level Signals Used

### 1. Relative Strength
Stocks with stronger performance relative to peers receive a higher score.

Why it matters:
Strong stocks tend to continue attracting attention, especially when supported by sector strength.

### 2. Price vs VWAP
The dashboard checks whether price is above or below VWAP.

Why it matters:
VWAP helps identify intraday strength and whether price is holding above a fair participation zone.

### 3. Intraday Price Change
Live price change is included in the stock scoring logic.

Why it matters:
Helps identify names showing momentum during the session.

### 4. Range Position
The dashboard checks where current price sits within the day’s range.

Why it matters:
Stocks near the upper end of the day’s range usually show better intraday strength than stocks trading weakly near the low.

### 5. Volume and Volume Ratio
Volume behavior is used to identify whether a move is supported by participation.

Why it matters:
A stock rising without participation is weaker than a stock rising with stronger-than-normal volume.

### 6. RSI-style momentum filters
Momentum quality filters help avoid weak or overstretched setups.

Why it matters:
This adds discipline to stock selection and reduces noise.

### 7. Risk Percentage
The dashboard calculates risk percentage based on entry and stop-loss logic.

Why it matters:
This makes the output more actionable and helps compare opportunities on a risk-aware basis.

## Sector-Level Logic

The dashboard does not evaluate stocks in isolation.

It also calculates sector-level strength based on:
- strength of top stocks in the sector
- count of strong names in the sector
- number of watch and trade-ready stocks in the sector

Why it matters:
Strong stocks often come from strong sectors. Sector context improves decision quality.

## Grade System

Stocks are classified into practical categories such as:
- Watch
- Watch+
- Trade Ready
- A
- A+

Why it matters:
A grade system helps the analyst quickly prioritize which names deserve immediate attention.

## Trade Ready Logic

A stock becomes more actionable when multiple factors align, such as:
- strong relative strength
- supportive sector
- healthy intraday structure
- acceptable risk profile
- better price behavior vs VWAP
- supportive volume

The dashboard uses these factors together rather than relying on one signal only.

## Strength of Current Version

The current version is strongest as:
- a live stock screening dashboard
- a technical and sector ranking tool
- a research workflow support tool
- a fast way to identify leaders during market hours

## What Will Be Added Next

The next version should add a stronger fundamental layer using:
- revenue growth
- earnings growth
- margin trends
- ROE
- ROCE
- debt to equity
- P/E and other valuation metrics
- quality of business and earnings consistency

## Analyst Value

This methodology is useful because it turns scattered market information into a repeatable process.

It helps an analyst move from:
raw data -> structured ranking -> focused research -> better decision-making
