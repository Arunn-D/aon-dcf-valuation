# Aon plc – DCF & Trading Comps Valuation Model

**Author:** Arun Drubhra  
**Date:** June 2026  
**Subject Company:** Aon plc (NYSE: AON)  
**Sector:** Professional Services / Insurance Advisory  
**Currency:** USD (millions unless stated)

---

## Overview

This is a full equity valuation model for Aon plc, one of the world's largest professional services firms operating across risk advisory, reinsurance, health, and wealth solutions. The model uses two independent valuation methodologies: Discounted Cash Flow (DCF) analysis and a Trading Comparables analysis.

The model was built in Excel using Python, taking dating from Aon's 2025 Annual Report / 10-K, Bloomberg consensus estimates, and public filings from peer companies.

---

## Model Structure

| Sheet | Contents |
|---|---|
| Cover | Title page, sheet index, colour coding key |
| Assumptions | All model inputs: revenue growth, margins, WACC components, terminal growth rate |
| Income Statement | FY2022A–FY2024A actuals; FY2025E–FY2029E projections |
| FCF Build | NOPAT → D&A → Capex → Working Capital → Unlevered Free Cash Flow |
| DCF Valuation | Discount factors, PV of FCFs, terminal value, EV bridge, implied share price |
| Sensitivity | 9×5 matrix of implied price across WACC (8–12%) and terminal growth rate (1.5–3.5%) |
| Trading Comps | Peer EV/EBITDA and P/E multiples; implied Aon share price from comps |
| Football Field | Visual summary of valuation range across all methods |

---

## Colour Coding

- **Blue text**: hardcoded inputs (change these to run scenarios)
- **Black text**: formulas and calculations
- **Green text**: links pulling from other sheets
- **Yellow fill**: key assumptions requiring attention

---

## Key Assumptions

| Assumption | Value | Rationale |
|---|---|---|
| Revenue Growth (FY2026E) | 5.5% | Consensus mid-single digit; NFP fully integrated |
| EBITDA Margin (projected) | 33.0% | Slight improvement on FY2025A (32.4%); consistent with management guidance |
| WACC | ~9.0% | Beta 1.05x, ERP 5.5% (Damodaran), RFR 4.3% (10yr UST), Kd 5.2% |
| Terminal Growth Rate | 2.5% | Conservative; in line with nominal long-run GDP growth |
| Net Debt | $8,200mm | Per Aon 2025 10-K (total debt $15.2bn less cash) |
| Shares Outstanding | 214mm | Per Aon 2025 10-K |

---

## Investment Thesis

### View: Aon is approximately fairly valued with modest upside potential

**Bull case - reasons to be positive:**

Aon is a high-quality, asset-light business generating consistent mid-30s EBITDA margins with strong free cash flow conversion. The 2024 acquisition of NFP (a middle-market benefits and insurance distributor) significantly expands Aon's addressable market in a segment growing faster than its core commercial risk business. Management has guided for meaningful revenue and margin synergies from NFP over the next three years, which are not yet fully reflected in consensus estimates.

The professional services advisory sector benefits from structural tailwinds: increasing complexity in risk (cyber, climate, geopolitical), rising demand for sophisticated reinsurance solutions, and growing corporate spend on employee health and benefits. Aon's global scale and distribution relationships create a durable competitive moat that smaller competitors cannot easily replicate.

Aon has also demonstrated consistent capital return discipline — returning capital via buybacks at a pace that has reduced the share count materially over the past decade — which acts as a reliable earnings-per-share growth driver even in periods of flat organic revenue growth.

**Bear case - key risks:**

At ~16.5x forward EV/EBITDA, Aon trades at a meaningful premium to its historical average and broadly in line with Marsh McLennan, its closest peer. Much of the NFP synergy story is already priced in. If integration proves more complex or slower than guided — a real possibility given NFP's decentralised operating model — the multiple could compress.

Aon carries significant financial leverage following the NFP acquisition, with net debt of approximately $9.8bn against an equity value of ~$71bn. In a rising rate environment, refinancing risk and interest cost creep are genuine headwinds. A recession scenario would likely see lower M&A activity and reduced corporate insurance spend, pressuring organic revenue growth.

The company also faces execution risk on its broader Aon Business Services platform — an initiative to centralise and standardise back-office operations globally. Cost overruns or client service disruptions during implementation could weigh on margins in the near term.

**Conclusion:**

The DCF base case (WACC 9.0%, TGR 2.5%) implies a share price broadly consistent with current trading levels (~$322), suggesting the market is pricing Aon efficiently. The trading comps analysis similarly points to a fair-value range of approximately $360–$430, with the stock sitting near the midpoint.

The risk/reward is modestly positive for a long-term holder willing to give management time to realise NFP synergies, but there is limited margin of safety at current prices. A more attractive entry point would be on any near-term weakness tied to integration concerns or macro headwinds.

**Implied price range across methodologies:**

| Method | Low | Base / Mid | High |
|---|---|---|---|
| DCF (base case) | — | ~$322 | — |
| DCF (sensitivity range) | ~$290 | — | ~$520 |
| EV/EBITDA comps | ~$350 | ~$380 | ~$410 |
| P/E comps | ~$340 | ~$370 | ~$400 |
| 52-week trading range | $305 | — | $415 |

---

## Data Sources

- Aon plc 2024 Annual Report / Form 10-K (SEC EDGAR)
- Aon plc 2023 Annual Report / Form 10-K (SEC EDGAR)
- Bloomberg / FactSet consensus estimates (June 2026)
- Damodaran Online — Equity Risk Premium (US, January 2025)
- Peer company filings: MMC, WTW, AJG 10-Ks

