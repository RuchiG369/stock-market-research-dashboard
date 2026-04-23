# Live Stock Research Dashboard

A practical stock market research dashboard for Indian equities that helps identify strong stocks, leading sectors, and trade-ready names using live market data, technical signals, ranking logic, and analyst-focused decision support.

## Why I Built This

This project was built as a live research and screening tool for Indian equities.

The goal is to reduce manual stock scanning and convert raw market data into structured research output that an analyst can use quickly during market hours.

Instead of checking many stocks one by one, the dashboard helps answer:

- Which sectors are leading right now?
- Which stocks are strongest within those sectors?
- Which names are trade-ready?
- What are the possible entry, stop loss, target, and risk levels?

## What the Dashboard Does

The dashboard:

- fetches live intraday market data
- ranks stocks using defined scoring logic
- scores sectors based on the strength of underlying stocks
- highlights top-ranked names
- shows trade-ready candidates
- presents analyst-friendly output in a simple dashboard layout

## Key Analysis Factors Used

This version is primarily a live screening and ranking dashboard. It is currently stronger on technical and market-structure analysis, with fundamental expansion planned next.

### Technical and screening factors
- Relative Strength
- Price vs VWAP
- Intraday Price Change
- Range Position
- Volume and Volume Ratio
- RSI-style momentum filters
- Sector Strength
- Grade system such as Watch, Watch+, Trade Ready, A, A+

### Fundamental layer planned next
- Revenue Growth
- Profit Growth
- EPS Growth
- ROE
- ROCE
- Debt to Equity
- P/E and valuation filters
- Earnings quality checks

## Dashboard Sections

### Top Summary Cards
Shows:
- 1st Best Stock
- 2nd Best Stock
- Best Sector

### Trade Ready Table
Shows:
- symbol
- sector
- grade
- entry
- stop loss
- target
- risk %
- RS rating

### Sector Leaders
Shows the leading stocks inside each sector so the analyst can understand both stock-level strength and sector context.

## Workflow

1. Live market data is fetched from the broker API
2. Stocks are mapped to sectors
3. Stock-level signals are calculated
4. Sector-level strength is calculated
5. Stocks are ranked using a defined scoring model
6. Results are saved to output files
7. Dashboard reads the latest output and refreshes automatically

## Analyst Use Case

This dashboard is designed as a decision-support tool for a stock market research analyst.

It helps:
- reduce manual scanning time
- identify leaders faster
- validate strong setups using multiple factors
- monitor sector rotation
- convert research into decision-ready output

## Product Testing Angle

This project is not only about stock analysis. It also reflects how I think as a product-minded analyst.

For a stock research platform, I believe a strong user should be able to:
- validate the quality of output
- identify gaps in ranking logic
- test whether the tool is useful in a real market workflow
- provide structured feedback on what works and what should improve

That mindset is reflected in this project through the dashboard, ranking model, and supporting notes included in this repository.

## Screenshots

Add your dashboard screenshots here

### Main Dashboard
![Main Dashboard](./screenshots/dashboard-main.png)

### Sector Leaders View
![Sector Leaders](./screenshots/dashboard-sectors.png)

## Repository Files

- `README.md`  
  Project overview and positioning

- `methodology.md`  
  Explains scoring logic, workflow, and analysis approach

- `sample_product_feedback.md`  
  Example of structured product feedback for a stock research platform

- `sample_stock_research_note.md`  
  Example of how a screened stock can be converted into a research note

- `benchmark_validation_note.md`  
  Example of validating tool output against manual analyst checks

## Tech Stack

- Python
- Pandas
- Upstox API
- Local dashboard server
- CSV output pipeline
- macOS automation for scheduled updates

## Setup

### 1. Clone the repository
```bash
git clone https://github.com/RuchiG369/live-stock-research-dashboard.git
cd live-stock-research-dashboard
