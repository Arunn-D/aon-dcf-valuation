# Aon plc (NYSE: AON) — Financial Valuation Model

**Author:** Arun Drubhra  
**Date:** April 2026  
**Tools:** Excel, Python  

---

## Executive Summary
Dual-method equity valuation model for Aon plc (NYSE: AON) combining a 5-year Unlevered Free Cash Flow (UFCF) Discounted Cash Flow (DCF) model and a Trading Comparables analysis (EV/EBITDA, P/E). Financials were extracted from Aon’s 2025 Form 10-K, adjusted for the NFP acquisition, and combined with market consensus data.

---

## Model Architecture
* **Cover:** Sheet index, navigation links, and standardized color-coding key.
* **Assumptions:** Central driver dashboard for revenue growth, operating margins, working capital assumptions, and WACC components.
* **Financial Statements:** Historical (FY22A–FY24A) and projected (FY25E–FY29E) Income Statement and Free Cash Flow build.
* **DCF Valuation:** Discount factors, Terminal Value (perpetuity growth), Enterprise Value to Equity Value bridge.
* **Sensitivity Analysis:** 9×5 matrix evaluating implied equity value across WACC (8.0%–12.0%) and Terminal Growth Rates (1.5%–3.5%).
* **Trading Comparables:** Multiples-based valuation benchmarked against primary peers: Marsh McLennan (MMC), Willis Towers Watson (WTW), and Arthur J. Gallagher (AJG).
* **Football Field Summary:** Aggregate chart displaying valuation ranges across DCF, sensitivity, and trading comps against 52-week trading bounds.

### Modeling Conventions & Standardized Formatting
* **Blue Text:** Hardcoded operational and market inputs.
* **Black Text:** Formulas and dynamic calculations.
* **Green Text:** Inter-sheet references and cross-linked variables.
* **Yellow Highlight:** Key scenario drivers.

---

## Core Valuation Assumptions

| Driver | Value | Rationale / Source |
| :--- | :--- | :--- |
| **FY26E Revenue Growth** | 5.5% | Mid-single digit organic growth + full NFP integration |
| **Projected EBITDA Margin** | 33.0% | Historical base (32.4% FY25A) + projected NFP cost synergies |
| **WACC** | ~9.0% | Risk-Free Rate: 4.3% (10Y UST), ERP: 5.5% (Damodaran), Beta: 1.05x, Kd: 5.2% |
| **Terminal Growth Rate** | 2.5% | Standard long-run nominal GDP growth proxy |
| **Net Debt** | $8,200M | Total Debt ($15.2B) less Cash ($7.0B) per 2025 10-K |
| **Diluted Shares** | 214M | Diluted share count per 2025 10-K |

---

## Valuation Summary & Findings

* **DCF Base Case Implied Price:** **~$322** (WACC: 9.0%, TGR: 2.5%).
* **DCF Sensitivity Range:** **$290 – $520** across 8.0%–12.0% WACC and 1.5%–3.5% TGR.
* **EV/EBITDA Comps Fair Value:** **$350 – $410** (Peer Median ~16.5x).
* **P/E Comps Fair Value:** **$340 – $400**.
* **52-Week Range:** **$305 – $415**.

**Analyst Take:** Base case DCF aligns closely with current trading levels (~$322), reflecting an efficiently priced market anchor. Upside potential depends on management executing NFP integration cost synergies faster than baseline guidance, while primary risks center on elevated debt service costs and macro softness in commercial line renewals.

---

## Data Sources
* SEC EDGAR: Aon plc 2024 & 2025 Form 10-K
* SEC EDGAR: Peer 10-K Filings (MMC, WTW, AJG)
* Damodaran Online: US Equity Risk Premium Data
* Market Consensus Data (June 2026)

