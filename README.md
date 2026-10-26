# Aon plc (NYSE: AON) — Equity Valuation Model

**Author:** Arun Drubhra  
**Degree:** BSc Mathematics with Economics, Loughborough University  
**Tools:** Excel, Python  

---

## Project Overview
I built a financial model for Aon plc (NYSE: AON) combining a 5-year Discounted Cash Flow (DCF) model and a Trading Comparables analysis against key industry peers (Marsh McLennan, Willis Towers Watson, Arthur J. Gallagher). 

The goal was to project Aon's cash flows, calculate an implied share price, and run sensitivity checks on key inputs like WACC and terminal growth rates.

Data was pulled from Aon's 2025 10-K filing, consensus estimates, and peer public filings.

---

## What's in the Model
* **Assumptions:** Input dashboard for revenue growth, margins, discount rates, and net debt.
* **Income Statement & FCF Build:** 3-year historical figures (FY22–FY24) and 5-year projections (FY25–FY29) to calculate Unlevered Free Cash Flow.
* **DCF Valuation:** Discount factors, perpetuity growth calculation, and Enterprise Value to Equity Value bridge.
* **Sensitivity Matrix:** 9×5 grid testing implied share prices across WACC (8%–12%) and Terminal Growth Rates (1.5%–3.5%).
* **Trading Comps:** Peer EV/EBITDA and P/E valuation multiples compared against Aon.
* **Football Field Summary:** Bar chart comparing price ranges across all valuation methods against the 52-week high/low.

---

## Key Model Inputs

| Input | Value | Notes / Source |
| :--- | :--- | :--- |
| **FY26 Revenue Growth** | 5.5% | Organic growth + NFP integration |
| **EBITDA Margin** | 33.0% | Slight increase on FY25 (32.4%) from expected NFP synergies |
| **WACC** | ~9.0% | Risk-Free Rate: 4.3%, ERP: 5.5%, Beta: 1.05x, Debt Cost: 5.2% |
| **Terminal Growth Rate** | 2.5% | Standard long-run GDP growth proxy |
| **Net Debt** | $8,200M | Total Debt ($15.2B) minus Cash ($7.0B) per 2025 10-K |
| **Shares Outstanding** | 214M | 2025 10-K |

---

## Valuation Summary

* **DCF Base Case Implied Price:** **~$322**
* **DCF Sensitivity Range:** **$290 – $520**
* **EV/EBITDA Peer Comps (16.5x median):** **$350 – $410**
* **P/E Comps:** **$340 – $400**
* **52-Week Range:** **$305 – $415**

### Summary Takeaway
The DCF base case (~$322) lands very close to where Aon is currently trading, which suggests the market has priced Aon fairly. The main upside potential comes from Aon cutting costs faster than expected after acquiring NFP. The main downside risks are higher interest payments on their debt and potential slowdowns in corporate insurance spend.

---

## Standard Model Color Coding
* **Blue text:** Hardcoded numbers and inputs
* **Black text:** Formulas and calculations
* **Green text:** Links to other sheets
* **Yellow fill:** Key assumptions to change for scenario testing

---

## Data Sources
* Aon plc 2024 & 2025 10-K Filings (SEC EDGAR)
* Peer Filings: MMC, WTW, AJG
* Damodaran Equity Risk Premium Data

