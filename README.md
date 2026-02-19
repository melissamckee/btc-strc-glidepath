# BTC/STRC Glide Path Calculator

A single-page tool for Bitcoin holders who need income. No pitch, no advice — just the numbers.

## The Problem It Solves

You hold Bitcoin. You believe in it long-term. But at some point you need monthly income — and Bitcoin doesn't pay dividends.

Strategy Inc's STRC preferred shares offer 11.25% annual yield (paid monthly, ~$0.94/share) with indirect Bitcoin exposure. The question isn't *whether* to consider it — it's **how much do you need, and what does it cost you in BTC?**

This calculator answers that question.

## How It Works

**① The Destination** — Start with what you need: total monthly income, minus what's already covered by Social Security, pensions, etc. The calculator shows the gap STRC must fill and exactly how many shares that requires.

**② Where You Are** — Enter your current BTC holdings (with cost basis for tax math), any STRC you already own, and your age. Age sets the projection horizon — a 50-year-old sees 35 years, a 70-year-old sees 15.

**③ How You Get There** — Two lanes, because real people don't convert on a schedule:

- **Lane A (DCA):** Monthly cash purchases of STRC. Supports multiple phases — e.g., $500/mo now, $1,000/mo after Social Security kicks in.
- **Lane B (Price Triggers):** Sell a percentage of your BTC stack when it hits specific prices. Each trigger sells from the *remaining* stack, not the original — so the math compounds correctly.

## What It Shows You

- **Progress bar** breaking down how much of your target comes from existing shares, DCA, and price triggers
- **Tax impact** of each BTC conversion (federal LTCG rates, state taxes for 10 jurisdictions, optional NIIT)
- **Price Trigger Waterfall** — a row-by-row table showing BTC sold, proceeds, tax owed, net STRC purchased, and running totals at each trigger level
- **"What Does the Target Cost You in BTC?"** — at $100K, $150K, $250K, $500K, $1M per BTC, how much of your stack funds the full income target
- **DCA timeline** — how many years DCA alone takes vs. DCA + triggers combined
- **ROC basis depletion** — how many years before return-of-capital treatment runs out and dividends become taxable
- **50% crash stress test** — what happens to your portfolio and income if BTC drops by half
- **Journey chart** — monthly income growth over time, showing DCA-only vs. triggers+DCA paths against your target line

## Tax Modeling

- Federal long-term capital gains: 0%, 15%, or 20%
- State capital gains for CA, NJ, NY, OR, MN, MD, VA, MA, IL, CO (or none)
- Optional NIIT (+3.8%) for high earners
- Tax is deducted from trigger proceeds *before* calculating STRC shares purchased — because the IRS gets paid first
- STRC dividends modeled as 100% return of capital (current treatment, expected 10+ years per Strategy Inc filings)

## Risks — Not Buried

The calculator displays these prominently, not in fine print:

- **Counterparty risk:** Depends entirely on Strategy Inc solvency
- **Junior position:** STRC is below STRF and all debt in liquidation — could receive zero
- **Variable rate:** The board can reduce the dividend at will
- **ROC is temporary:** If Strategy generates earnings & profits, dividends become taxable
- **Reserve runway:** $2.25B covers ~2.5 years of all preferred dividends
- **Not insured:** Not FDIC, not a bank deposit, not Treasuries

## Live Data

Fetches real-time BTC price from CoinGecko API on load. All calculations update instantly as you adjust any input.

## Usage

It's a single HTML file. No build step, no dependencies to install.

1. Download `btc-strc-glidepath-v4.html`
2. Open it in any modern browser
3. Adjust the inputs to match your situation

Or host it via GitHub Pages and share the link.

## Background

Built through iterative collaboration between a human (who understands the problem firsthand) and AI assistants (Grok for the initial prototype, Claude for the redesign). The key insight that shaped the final version: **start from the destination (income needed), not the portfolio (percentage to convert).** Real investors don't rebalance on a calendar — they sell into strength at price levels they've thought about in advance.

## Disclaimer

Modeling tool only. Not financial, tax, or investment advice. Tax estimates are simplified — consult a professional. STRC data as of February 2026.
