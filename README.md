# Family Budget Calculator — Spain 2026

[![GitHub Pages](https://img.shields.io/badge/Live%20demo-GitHub%20Pages-brightgreen?logo=github)](https://konradcinkusz.github.io/IberiaFamilyCalculator/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.txt)

A configurable family budget calculator with real Spanish tax math (IRPF, autónomos, payroll). Built for families making big decisions — relocation, going freelance, switching companies, taking a sabbatical.

**🔗 Live demo:** [konradcinkusz.github.io/IberiaFamilyCalculator](https://konradcinkusz.github.io/IberiaFamilyCalculator/)

**📦 Repository:** [github.com/konradcinkusz/IberiaFamilyCalculator](https://github.com/konradcinkusz/IberiaFamilyCalculator)

**Three languages:** Spanish · Polish · English (switcher in the top-right corner).

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

The app is already live at **[konradcinkusz.github.io/IberiaFamilyCalculator](https://konradcinkusz.github.io/IberiaFamilyCalculator/)**.

To deploy your own fork:

1. Fork or clone the repository.
2. Go to **Settings → Pages**, select branch `main`, folder `/ (root)`.
3. Within seconds your copy is live at `https://YOUR-USER.github.io/IberiaFamilyCalculator/`.

> **Note:** `index.html` is fully self-contained. Fonts are self-hosted in `fonts/` — no external CDN requests.

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

## Privacy & cookies

**No cookie banner is needed.** This app:

| What | How | GDPR |
|---|---|---|
| User config | `localStorage` (functional) | ✅ No consent needed |
| Shared scenarios | URL fragment (`#hash`) | ✅ Never sent to a server |
| Analytics / tracking | None | ✅ N/A |
| Fonts | Self-hosted in `fonts/` | ✅ No third-party requests |

Fonts are **self-hosted** (not loaded from `fonts.googleapis.com`), which eliminates the Google Fonts GDPR concern raised in the [LG München I ruling (2022)](https://gdprhub.eu/index.php?title=LG_M%C3%BCnchen_I_-_3_O_17493/20) regarding IP address transfers to US servers without consent.

The app has no backend, no tracking, and no cookies of any kind.

## Disclaimer

A first-visit disclaimer popup is built into the app. It appears once per browser (stored in `localStorage`) and covers:

- The indicative, non-advisory nature of the calculations
- Known limitations (no regional deductions, no Beckham regime, foral approximations)
- A prompt to consult a qualified tax advisor for important decisions



This calculator is **indicative**. It does not replace a tax advisor. Specifically:

- Region-specific deductions (primary residence, young-renter relief, donations, large families, etc.) are not included.
- The Beckham regime (special expat scheme) is not modelled.
- Basque Country and Navarre use their own foral system — values here are reasonable approximations, but exact computation requires the foral scales updated annually.
- The autónomos quota is computed iteratively and may differ slightly from official Social Security numbers.
- IRPF brackets can be amended mid-year by ad-hoc decrees.

For big decisions, validate the numbers with an advisor.

## License

The calculator code is **MIT** — see [`LICENSE.txt`](LICENSE.txt).

The fonts in `fonts/` are licensed under the **SIL Open Font License 1.1** — see [`fonts/OFL-LICENSE.txt`](fonts/OFL-LICENSE.txt):
- [Cormorant Garamond](https://github.com/CatharsisFonts/Cormorant) © 2015 The Cormorant Garamond Project Authors
- [DM Sans](https://github.com/googlefonts/dm-fonts) © 2014–2022 The DM Sans Project Authors

OFL permits free use, redistribution and self-hosting. The font files may not be sold standalone.
