# Residential solar payback by US state (2026)

How many years a home solar system takes to pay for itself in each of the 50 US states, and what it saves over
25 years, for a home with a **$150 monthly electricity bill**, bought with cash and **without the federal tax credit**.

Interactive version, method and state-by-state notes: **[Solar by State, best states for solar 2026](https://solarbystate.com/best-states-for-solar/)**.

| Rank | State | Simple payback | 25-year net savings |
|---|---|---|---|
| 1 | Hawaii | 8.04 years | $16,203 |
| 2 | Massachusetts | 8.58 years | $26,959 |
| 3 | Maine | 9.39 years | $25,507 |
| 4 | Rhode Island | 9.43 years | $25,433 |
| 5 | Connecticut | 10.34 years | $20,461 |

Full table: [`data/solar-payback-by-state-2026.csv`](data/solar-payback-by-state-2026.csv) (50 rows, checked 2026-10-08).

## Columns

| Column | Meaning |
|---|---|
| `rank` | 1 = fastest payback |
| `state`, `code` | State name and postal code |
| `payback_years` | Years until cumulative savings equal the system cost |
| `net_savings_25y_usd` | Savings over 25 years minus the system cost (negative = it does not pay back in 25 years) |
| `system_kw` | System size that covers the bill, in kW |
| `system_cost_usd` | `system_kw` × installed cost per watt |
| `year1_savings_usd` | Bill savings in the first year |
| `price_cents_kwh` | Residential electricity price, ¢/kWh |
| `kwh_per_kw_year` | Yearly output of 1 kW of panels in the city shown |
| `city` | City used for the solar output |
| `cost_per_w_usd` | Median installed price, $/W |
| `cost_is_state_median` | `true` = state median from Berkeley Lab; `false` = US median used because the state sample is small |
| `export_rule` | How the state credits power sent to the grid: `net-metering`, `net-billing` or `utility-specific` |
| `solar_kwh_value_pct_of_retail` | Average value of a solar kWh as a share of the retail price, after export credits |

## Sources

- Electricity prices: [EIA Electric Power Monthly, table 5.6.B](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_5_6_b), residential average, July 2026 year to date.
- Solar output: [PVGIS 5.2](https://re.jrc.ec.europa.eu/pvg_tools/en/) (European Commission Joint Research Centre) with NSRDB radiation data; 1 kW, fixed, south-facing, 20° tilt, 14% system losses, 2005–2015 average.
- Installed cost: [Berkeley Lab, Distributed Solar & Storage: 2026 Data Update](https://emp.lbl.gov/sites/default/files/2026-08/Distributed%20Solar%20%26%20Storage-2026%20Data%20Update_FINAL.pdf), median price of host-owned residential systems installed in 2025.
- Export rules: each state's utility commission or law, listed on the [state pages](https://solarbystate.com/).

Full method: [how we calculate solar payback](https://solarbystate.com/how-we-calculate-solar-payback/).

## Limits

These are planning estimates, not quotes. Real payback depends on the roof, shading, utility tariff and the price an
installer offers. Electricity prices change every month; the website is refreshed monthly and this repository is a
snapshot as of 2026-10-08.

## License and citation

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Reuse freely with a link to the source:

```html
Source: <a href="https://solarbystate.com/best-states-for-solar/">Solar by State, best states for solar 2026</a>
```
