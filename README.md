# Aon plc (NYSE: AON) - Equity Valuation Model

**Author:** Arun Drubhra  
**Degree:** BSc Mathematics with Economics, Loughborough University  
**Tools:** Excel, Python  

---

## Project Overview
A dual-method financial model for Aon plc (NYSE: AON) combining a 5-year Discounted Cash Flow (DCF) model and a Trading Comparables analysis against primary peers (Marsh McLennan, Willis Towers Watson, Arthur J. Gallagher).

The model projects Aon's free cash flows, computes an implied share price, and evaluates valuation sensitivity across varying WACC and Terminal Growth Rate scenarios.

Data was sourced from Aon's 2025 Form 10-K, peer SEC filings, Bloomberg consensus data, and Damodaran cost of capital estimates.

---

## Model Structure
* **Cover:** Sheet index, navigation, and standard color-coding guide.
* **Assumptions:** Driver inputs for revenue growth, EBITDA margins, working capital, and WACC components.
* **Income Statement & FCF Build:** FY23A–FY25A actuals and FY26E–FY30E projections deriving Unlevered Free Cash Flow (UFCF).
* **DCF Valuation:** WACC derivation, discount factors, Gordon Growth terminal value, and Enterprise Value to Equity Value bridge.
* **Sensitivity Analysis:** 9×5 grid testing implied share prices across WACC (8.0%–12.0%) and Terminal Growth Rates (1.5%–3.5%).
* **Trading Comps:** Peer EV/EBITDA and P/E valuation multiples benchmarked against Aon.
* **Football Field Summary:** Aggregate chart displaying valuation bounds across all methodologies against the 52-week trading range.

---

## Key Model Inputs & WACC Build

| Assumption / Component | Model Input | Source / Note |
| :--- | :--- | :--- |
| **FY26E Revenue Growth** | 5.5% | Consensus estimate (~6% base organic growth) |
| **Projected EBITDA Margin** | 33.0% | Slight expansion on FY25 (32.4%) driven by NFP integration synergies |
| **Risk-Free Rate (10Y UST)** | 4.30% | Macro benchmark rate |
| **Equity Risk Premium (ERP)** | 5.50% | Damodaran US ERP benchmark |
| **Beta** | 1.05x | 5-year monthly Bloomberg beta vs S&P 500 |
| **Calculated WACC** | **7.85%** | Cost of Equity (10.08%) × 62% + After-tax Cost of Debt (4.21%) × 38% |
| **Terminal Growth Rate (TGR)** | 2.50% | Long-term nominal GDP growth proxy |
| **Net Debt** | $8,200M | Total Debt ($15.2B) less Cash ($7.0B) per 2025 10-K |
| **Diluted Shares** | 214M | 2025 10-K share count |

---

## Valuation Results

* **DCF Base Case Implied Price (7.85% WACC, 2.5% TGR):** **$388.96**
* **DCF Conservative Scenario (9.00% WACC, 2.5% TGR):** **$312.50**
* **DCF Sensitivity Range (8%–12% WACC, 1.5%–3.5% TGR):** **$184.36 – $452.62**
* **EV/EBITDA Comps (14.8x – 15.2x multiples):** **$345.24 – $354.57**
* **P/E Comps (22.5x – 24.3x multiples):** **$370.09 – $399.04**
* **52-Week Trading Range:** **$305.00 – $381.00** *(Current market ~$322)*

### Valuation Takeaway
The base case DCF indicates an implied share price of **$388.96** based on Aon's target WACC of 7.85%. Under a conservative rate scenario (WACC rising to 9.0%), the implied price drops to **$312.50**, aligning closely with current market trading levels (~$322). Trading comps suggest a fair-value range between **$345 and $399**, highlighting that market valuation currently prices in modest downside macro risks while leaving room for upside if NFP integration synergies outperform baseline guidance.

---

## Standard Model Formatting
* **Blue text:** Hardcoded inputs and scenario parameters
* **Black text:** Dynamic formulas and calculations
* **Green text:** Cross-sheet links
* **Yellow highlight:** Key scenario drivers

---

## Data Sources
* SEC EDGAR: Aon plc 2024 & 2025 Form 10-K
* SEC EDGAR: Peer 10-K Filings (MMC, WTW, AJG)
* Damodaran Online: US Equity Risk Premium Data

