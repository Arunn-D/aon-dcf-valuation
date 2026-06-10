# Plain English Guide to the Aon DCF Model
### What every part does and why it matters — no finance background needed

---

## The Big Picture: What is this model trying to do?

The model is trying to answer one question: **is Aon's share price fair?**

Aon's shares trade on the New York Stock Exchange. On any given day the market says they're worth roughly $388 each. But is that actually the right price — or is the company worth more or less than that?

To figure this out, we build a model that estimates what Aon is *intrinsically* worth based on the cash it's expected to generate in the future. We then compare that estimate to the current price. If our estimate is higher than $388, the stock might be cheap. If it's lower, it might be expensive.

We do this two different ways — a DCF analysis and a Trading Comps analysis — and then display both answers side by side in a Football Field chart. Using two methods is important because each one has weaknesses; if both point to roughly the same answer, you can be more confident.

---

## Sheet 1: Cover

This is just a title page. In a real investment bank or advisory firm, every piece of work goes out with a cover page showing the company name, date, analyst name, and a brief description of what's inside. It's professional presentation, nothing more.

The colour coding key at the bottom is important though — it tells you what the different text colours mean throughout the model:
- **Blue** = a number you typed in yourself (an assumption)
- **Black** = a number the spreadsheet calculated from a formula
- **Green** = a number pulled in from a different sheet in the same file
- **Yellow background** = a particularly important assumption worth reviewing

---

## Sheet 2: Assumptions

This is the control panel of the entire model. **Every key number that drives the projections lives here.** If you want to run a different scenario — say, what if Aon grows faster than expected? — you change a number on this sheet and everything else updates automatically.

**Revenue growth rates:** How fast do we expect Aon's sales to grow each year? We project 6.2% in 2025, slowing gradually to 5.0% by 2029. These are based on analyst consensus estimates and Aon's own guidance.

**EBITDA margin:** Out of every $1 of revenue Aon earns, how much is left over as profit before interest, tax, and accounting charges? We assume ~32%. This is a measure of how efficiently Aon runs its business.

**Capex (Capital Expenditure):** How much does Aon spend each year on physical assets like buildings, computers, and equipment? Aon is an advisory firm — it doesn't build factories — so this is a small 1.8% of revenue. This matters because money spent on capex can't be returned to shareholders.

**WACC (Weighted Average Cost of Capital):** This is the discount rate — arguably the most important single number in the model. It represents the return that investors *require* to justify investing in Aon rather than something safer. It's made up of:
- *Risk-free rate* — the return on a US government bond (basically "guaranteed" money, ~4.3%)
- *Equity risk premium* — the extra return investors demand for taking on stock market risk (~5.5%)
- *Beta* — how much Aon's share price moves relative to the overall market (1.05 means it moves slightly more than the market)
- *Cost of debt* — the interest rate Aon pays on its borrowings (~5.2%)

A higher WACC makes the company worth less (future cash flows are discounted more heavily). A lower WACC makes it worth more. This is why WACC is the key variable in the sensitivity analysis.

**Terminal growth rate:** After 2029, we don't project year by year forever. Instead we assume the business grows at a steady 2.5% forever — roughly in line with long-run economic growth. This assumption has an enormous impact on the final valuation.

---

## Sheet 3: Income Statement

This is a standard Profit & Loss statement — it shows how much money Aon makes and where it goes.

**Revenue** is total sales — the fees Aon charges clients for advisory, risk, and reinsurance services.

**EBITDA** stands for Earnings Before Interest, Tax, Depreciation and Amortisation. It's a measure of operating profit before accounting adjustments. It's widely used in finance because it's a cleaner measure of cash generation than net income.

**D&A (Depreciation & Amortisation)** is an accounting charge that spreads the cost of assets over their useful life. Aon spent $440mm on D&A in 2024. Crucially, *it isn't a real cash outflow* — no money leaves the business when D&A is charged. This is why we add it back later.

**EBIT** (Earnings Before Interest and Tax) = EBITDA minus D&A. This is operating profit.

**Interest Expense** is the cost of Aon's debt — the interest payments on its bonds and loans.

**Net Income** is the bottom line — what's left after everything.

The first three columns (FY2022A, FY2023A, FY2024A) are *actuals* — real numbers from Aon's published accounts. The remaining five columns are *projections* — our estimates of what these numbers will be.

---

## Sheet 4: FCF Build

FCF stands for **Free Cash Flow** — the actual cash the business generates that could theoretically be paid out to all investors (both shareholders and lenders).

This is the number that really matters in a DCF. We don't use net income because net income includes accounting distortions. Free cash flow strips those out.

Here's how it's built:

**EBIT** — operating profit (pulled from the income statement)

**Less: Taxes on EBIT** — we tax the operating profit directly, as if the company had no debt. This gives us a "debt-free" view of profitability.

**= NOPAT** (Net Operating Profit After Tax) — operating profit after tax, before any financing effects

**Add back: D&A** — we add this back because, as mentioned above, it's not a real cash outflow. The income statement deducted it, so we reverse it here.

**Less: Capex** — we subtract capital expenditure because that *is* a real cash outflow — money spent investing in the business.

**Less: Change in Working Capital** — working capital is the day-to-day cash tied up running the business (money owed by customers minus money owed to suppliers). As a business grows, it typically needs slightly more working capital, which is a small cash cost.

**= Unlevered Free Cash Flow** — the final number. This is the cash available to all investors before any debt payments.

---

## Sheet 5: DCF Valuation

This is where we turn those future cash flows into a single value today — the intrinsic value of the company.

**Why can't we just add up the cash flows?**

Because £100 today is worth more than £100 in five years' time. Money now can be invested and earn a return. So future cash flows need to be *discounted* — reduced in value — to reflect how much they're worth in today's money. That's what the WACC is for.

**Discount factor:** For each year, we calculate `1 / (1 + WACC)^n` where n is the number of years away. So FY2025 (1 year away) gets discounted by `1/(1.09)^1 = 0.917`. FY2029 (5 years away) gets discounted by `1/(1.09)^5 = 0.650`. Cash flows further in the future are worth less today.

**PV of FCFs:** Each year's free cash flow multiplied by its discount factor. Sum of all five years gives the total present value of the projection period cash flows.

**Terminal Value:** We can't project forever, but Aon will (presumably) keep generating cash after 2029. We capture this using the Gordon Growth Model:

> Terminal Value = Final year FCF × (1 + terminal growth rate) / (WACC − terminal growth rate)

This produces a single large number representing the value of all cash flows from 2030 onwards. We then discount it back to today as well.

**Enterprise Value (EV)** = PV of FCFs + PV of Terminal Value. This is the value of the whole business — as if it were owned outright with no debt.

**Equity Value** = Enterprise Value − Net Debt. We subtract the debt because debtholders have first claim on the business's assets. What's left belongs to shareholders.

**Implied Share Price** = Equity Value ÷ Shares Outstanding. Dividing the total equity value by the number of shares gives the value per share — the number we compare to the current market price.

---

## Sheet 6: Sensitivity Analysis

The DCF answer depends heavily on two assumptions: WACC and terminal growth rate. Small changes to either can move the implied price by $50–$100.

Rather than pretending our base case is exactly right, the sensitivity table shows the implied price across a wide range of WACC (8%–12%) and terminal growth rate (1.5%–3.5%) combinations. The base case is highlighted in yellow.

This is important because it shows the *range of reasonable outcomes* rather than a false single-point answer. In a real advisory context, you'd present this table to a client so they understand how sensitive the valuation is to the key inputs.

---

## Sheet 7: Trading Comps

The second valuation method. Instead of projecting cash flows, we ask: **what are similar companies trading at, and what does that imply for Aon?**

We look at five peer firms — Marsh & McLennan, Willis Towers Watson, Arthur J. Gallagher, Howden, and Lockton — and observe two key multiples:

**EV/EBITDA:** Enterprise value divided by EBITDA. If the average peer trades at 16x EBITDA, and Aon's EBITDA is $5bn, then a comparable valuation would put Aon's EV at $80bn. Subtract net debt to get equity value, divide by shares to get implied price.

**P/E (Price-to-Earnings):** Share price divided by earnings per share. If peers trade at 25x earnings and Aon earns $15 per share, the implied price is $375.

The logic is simple: if two nearly identical businesses exist, they should trade at similar multiples. If Aon is cheaper than its peers on these metrics, it might be undervalued — and vice versa.

The bottom section of this sheet translates the peer multiples directly into an implied Aon share price, which feeds into the Football Field.

---

## Sheet 8: Football Field

The Football Field chart is the standard way to present a valuation to a client or senior colleague. It gets its name from its appearance — horizontal bars that look a bit like a football field viewed from above.

Each bar represents one valuation method and shows the range of outcomes for that method:
- The left edge of the bar = the low-end implied price
- The right edge = the high-end implied price
- The midpoint marker = the base case

Laying all the methods on the same chart makes it easy to see where they agree (giving you more confidence) and where they diverge (flagging uncertainty). A vertical line showing the current share price (~$388) lets you instantly see whether the stock looks cheap or expensive relative to each method.

In practice at an investment bank or advisory firm, the Football Field is often the *first* thing an MD looks at when reviewing a valuation — it's the executive summary of all the analysis that went into the model.

---

## How it all connects

```
Assumptions sheet
      │
      ▼
Income Statement ──► FCF Build ──► DCF Valuation ──► Football Field
                                         │                   ▲
Trading Comps ───────────────────────────┘                   │
      └──────────────────────────────────────────────────────┘
```

Every number flows from the Assumptions sheet. Change one input there and the entire model — income statement, cash flows, DCF valuation, comps-implied prices, and the football field chart — updates automatically. That's what makes it a proper financial model rather than just a spreadsheet of numbers.

---

## Glossary of Key Terms

| Term | Plain English meaning |
|---|---|
| DCF | Discounted Cash Flow — valuing a company by estimating its future cash flows and discounting them to today |
| WACC | The required return on the company's capital — used as the discount rate |
| Free Cash Flow | The actual cash generated by the business available to all investors |
| EBITDA | A measure of operating profit before accounting charges |
| NOPAT | Operating profit after tax, before financing effects |
| Terminal Value | The value of all cash flows beyond the projection period, captured as a single lump sum |
| Enterprise Value | Total value of the business (equity + debt) |
| Equity Value | What belongs to shareholders = EV minus net debt |
| Trading Comps | Valuing a company by comparing it to similar listed peers |
| EV/EBITDA | A valuation multiple — how many times EBITDA the market values the company at |
| Football Field | A chart showing the valuation range from each method side by side |
| Beta | How much a stock moves relative to the overall market |
| Sensitivity Analysis | Testing how much the answer changes when you vary key assumptions |

---

*Built by Arun Drubhra — June 2026*
