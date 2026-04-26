# Family Budget Calculator — Spain 2026

A configurable family budget calculator with real Spanish tax math (IRPF, autónomos, payroll). Built for families making big decisions — relocation, going freelance, switching companies, taking a sabbatical.

**Three languages:** Spanish · Polish · English (switcher in the top-right corner).

**Live demo:** publish `index.html` to GitHub Pages and use it from any browser.

## Features

- **Dynamic entities.** Add as many payrolls, autónomos, benefits and expenses as you need. Each with its own slider, configurable bounds (min/max/step), editable name, duplicate and delete buttons.
- **Real per-region IRPF.** 2026 state brackets + autonomous brackets for Madrid, Catalonia, Valencia, Andalusia, Galicia, plus foral approximations for Basque Country and Navarre.
- **Personal & family minimums.** Applies the personal minimum and per-dependent minimums (with the under-3 bonus) correctly, split 50/50 for married declarants.
- **Tier-based autónomos quota.** 2026 progressive scale (RD 504/2022) — quota is calculated iteratively over net income.
- **Flexible compensation.** Tax-exempt benefits compute their real saving using your personalised marginal rate.
- **Triple persistence.** Your setup is saved in `localStorage` *and* in the URL hash — share your scenario by copying the link.
- **Export/import JSON.** Save scenarios, compare them, share by email.
- **Print / PDF.** Clean print stylesheet included.
- **Undo on delete.** Removed an entity by accident? A toast with "Undo" gives you 4 seconds to restore it.
- **Three languages.** Full UI translation with language saved per-user. Auto-detects browser language on first visit.
- **Zero dependencies.** Single static HTML file. No tracking, no cookies, no backend.

## How to publish on GitHub Pages

1. Create a new repository (e.g. `family-calculator`).
2. Upload `index.html` to the root.
3. In **Settings → Pages**, select branch `main`, folder `/ (root)`.
4. Within seconds your calculator is live at `https://YOUR-USER.github.io/family-calculator/`.

## How to use

### Family setup
Pick your Autonomous Community, number of dependent children, and how many are under 3. This directly affects IRPF math.

### Income
Three types:
- **Payroll (employee).** Annual gross, optional bonus %, number of pay periods (12, 14, or 16). Applies IRPF + Social Security at 6.35%.
- **Autónomo.** Annual gross + deductible-expenses percentage. Applies tier-based quota + IRPF.
- **Other.** Direct net amount (rents, dividends, passive income already taxed elsewhere).

### Benefits
In-kind benefits with tax advantage (meal vouchers, childcare, health insurance, transit, pension plan). Mark "IRPF-exempt" if applicable — the calculator estimates your tax saving using your marginal rate.

### Expenses
Fixed and variable monthly expenses. Each with a configurable slider.

### Side panel (live results)
- Net monthly income (with effective IRPF % and yearly figure)
- Benefits and estimated tax saving
- Total expenses
- Monthly balance
- 1-year, 3-year and 5-year projection

## Limitations

This calculator is **indicative**. It does not replace a tax advisor. Specifically:

- Region-specific deductions (primary residence, young-renter relief, donations, large families, etc.) are not included.
- The Beckham regime (special expat scheme) is not modelled.
- Basque Country and Navarre use their own foral system — values here are reasonable approximations, but exact computation requires the foral scales updated annually.
- The autónomos quota is computed iteratively and may differ slightly from official Social Security numbers.
- IRPF brackets can be amended mid-year by ad-hoc decrees.

For big decisions, validate the numbers with an advisor.

## License

MIT — use, modify, share freely.
