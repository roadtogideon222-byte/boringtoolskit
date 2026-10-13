# BoringToolsKit

> MCP server for free, private calculators: 36 tools that compute payments, APY, budgets, home projects, and everyday math directly in Claude with no accounts and no data leaving your session.

BoringToolsKit is a free collection of private, no-signup browser calculators and everyday tools for money, home, school, and work, built for anyone who wants instant answers without accounts or uploads.

Official site: https://boringtoolskit.com

## Tools

| Tool | Description |
|------|-------------|
| `tip_bill_split` | Split a bill across a group after tax, tip, and optional rounding. Returns each person's share, the tip, the effective tip rate, and the collected total. |
| `discount_percent_off` | Compute the final checkout total after stacked percentage discounts, a fixed coupon, and a tax assumption. Sequential discounts are NOT additive. |
| `bmi` | Calculate body mass index and category from weight and height in US units. |
| `bmr_tdee` | Estimate basal metabolic rate (Mifflin-St Jeor) and total daily energy expenditure from age, weight, height, sex, and an activity multiplier. |
| `mortgage_payment` | Estimate the full monthly housing payment (principal, interest, tax, insurance, PMI, HOA) and the total interest over the term. Requires a positive home price. |
| `auto_loan` | Estimate a monthly auto-loan payment from price, down payment, trade-in, term, and APR. |
| `compound_interest` | Grow a balance with compound interest and optional monthly contributions. Returns future value, total contributed, and interest earned. |
| `savings_growth` | Project the future value of a lump-sum investment (optionally with monthly additions), including interest earned. |
| `simple_interest` | Compute simple interest, total value, and a comparison to annual compounding. |
| `calorie` | Estimate BMR and total daily energy expenditure using Mifflin-St Jeor, from weight/height in US units. |
| `percentage` | Solve percentage problems: what is X% of Y, X is what % of Y, or the % change from X to Y. |
| `square_footage` | Compute total area (and with-waste area) from up to two rectangular spaces, plus square yards, square metres, and acres. |
| `apy` | Compute annual percentage yield from a nominal rate and a compounding frequency, plus the one year interest and ending balance on an example deposit. |
| `win_loss_percentage` | Compute a winning percentage from wins, losses, and ties, where ties count as half a win. |
| `slope` | Compute slope from rise and run as degrees, percent grade, and the rise to run ratio. Run must be above zero. |
| `rule_of_72` | Estimate the doubling time of money at a fixed rate using the rule of 72, plus the exact doubling time from the compound formula. Rate must be between 0 and 30 percent. |
| `cagr` | Compute the compound annual growth rate connecting a starting and an ending value over a number of years, with total return percent and absolute change. |
| `remainder` | Compute the remainder and floored quotient of a division. Works for decimal inputs, not just integers. |
| `combinations` | Compute the number of distinct combinations, n choose r, using a multiplicative form that avoids factorial overflow. |
| `margin_of_error` | Compute the margin of error for a survey sample at the 90, 95, or 99 percent confidence level, assuming maximum variance proportions. |
| `va_mortgage` | Monthly VA loan payment including the funding fee, with no PMI. Returns the financed amount, payment, and total interest. |
| `gross_rent_multiplier` | Gross rent multiplier for a rental property: price divided by annual gross rent. Lower means more rent per dollar of price. |
| `emergency_fund` | Emergency fund target (expenses times coverage months), the remaining gap versus current savings, and months to close the gap at a fixed monthly contribution. |
| `dividend_reinvestment` | Compound a portfolio with a constant dividend yield and price growth, reinvesting monthly and optionally adding deposits. Returns ending value, total contributed, and dividends reinvested. |
| `budget_50_30_20` | Split monthly after-tax income by the 50/30/20 rule into needs, wants, and savings or debt paydown. |
| `growing_degree_day` | Accumulate growing, heating, or cooling degree days (Fahrenheit basis) from daily high, low, a base threshold, and a day count. Includes Celsius-basis totals. |
| `insulation` | U-value of an insulation upgrade and an estimated annual heating saving from conduction, using heating degree days, area, kWh conversion, and utility cost. |
| `roofing` | Roof area from footprint and pitch, with waste allowance, roofing squares, and approximate shingle bundles (3 per square). |
| `maintenance_calories` | Daily maintenance calories (TDEE) from Mifflin-St Jeor BMR and an activity level, using metric inputs. |
| `protein_molecular_weight` | Estimate a protein chain molecular weight in Da and kDa from residue count and average residue mass, plus peptide bond count. |
| `key_transposition` | Transpose a musical key and report the number of semitone steps upward between two keys. |
| `audio_time_stretch` | Compute the new duration of audio at a playback speed, plus the percent time change. |
| `youtube_revenue` | Estimated YouTube Adsense revenue from monthly views and RPM, with an annual figure and a 30 percent RPM swing range. RPM defaults to 2 when omitted. |
| `ceiling_tile` | Count 2x2 ft ceiling tiles needed for a rectangular room, with room area and a 5 percent cut-waste reminder. |
| `boat_loan` | Boat or RV loan payment with optional sales tax, down payment, and trade-in, including amount financed and total interest. |
| `pressure` | Compute pressure in Pascals, kilopascals, and psi from a force in newtons over an area in square metres. |

Every tool carries `readOnlyHint: true`, so the server computes and returns numbers only. It never writes, never calls out to third parties, and never asks for an account.

## Installation

### Remote MCP (recommended, no install)

Add to `claude_desktop_config.json`, `mcp.json`, or your client's connector settings:

```json
{
  "mcpServers": {
    "boringtoolskit": {
      "url": "https://boringtoolskit.com/mcp"
    }
  }
}
```

Streamable HTTP transport, no authentication (the tools are public data). Works in Claude Desktop, Claude Code, Cursor, and any MCP client supporting remote servers.

### MCP endpoint

- URL: `https://boringtoolskit.com/mcp`
- Transport: Streamable HTTP
- Protocol: `2024-11-05` and `2025-06-18` tested
- Auth: none required (public read-only calculator tools)

## What's inside the site

The website ships 850+ lightweight browser tools that run entirely client-side. Nothing is uploaded, nothing requires an account:

- **Money**: loan/mortgage/payoff calculators, tip splitters, discount and tax calculators, salary and freelance rate tools
- **Home**: paint, flooring, BTU, energy-cost and DIY measurement calculators
- **School**: GPA calculators, grade trackers, unit converters, study timers
- **Work**: timesheet and invoice calculators, text utilities, date and timezone tools

## Privacy-first by design

- No signup, no email, no accounts
- No uploads: calculation happens client-side in your browser
- Free to use, unlimited
- Full policy: https://boringtoolskit.com/privacy/

## Links

- Website: https://boringtoolskit.com
- MCP endpoint: https://boringtoolskit.com/mcp
- Agent skills: https://boringtoolskit.com/skills/
- Machine-readable index: https://boringtoolskit.com/llms.txt
- Methodology: https://boringtoolskit.com/methodology/
