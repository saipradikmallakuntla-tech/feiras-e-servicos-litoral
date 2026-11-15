# Feiras e Serviços do Litoral / Coastal Markets and Services

[Aplicativo / Live app](https://saipradikmallakuntla-tech.github.io/feiras-e-servicos-litoral/)

PT: diretório demonstrativo com quatro registros fictícios, filtros de município/dia/categoria, busca sem distinção de acentos e simulador de orçamento. Interface, resultados e erros PT/EN. Não é agenda real nem lista de serviços verificados.

EN: demonstration directory with four fictional records, city/day/category filters, accent-insensitive search and a visit-budget simulator. PT/EN interface, results and validation. Not a real schedule or a verified service listing.

## Run / Executar

Static HTML/CSS/JS; no build, package dependency, API, analytics, geolocation or persistent form-data storage. Run `python3 -m http.server 8080`. Publish `main` root, `.nojekyll`, enforced HTTPS, no custom domain. `?lang=en` selects English. Ordinary HTML links work without JavaScript.

## Model / Modelo

Pure `core.js` exports `calculate`, `filter` and `records` for Node. Base = people × spending per person + total transport. Extra = base × reserve percentage. Total = base + extra; per-person share = total / people. Base, reserve, total and per-person share are rounded to cents. People must be an integer 1–50; spending 0–10,000 BRL; transport 0–100,000 BRL; reserve 0–100%. All must be finite. Defaults: 2 × 40 + 20, then 10% reserve = BRL 110, or BRL 55 each. These are entered example amounts, not market prices.

All days and entries are fictional. There are no verified addresses, opening hours or operational claims. Municipal starting points selected 2026-11-15: https://www.santos.sp.gov.br/ , https://www.guaruja.sp.gov.br/ , https://www.saovicente.sp.gov.br/ . Selection is not verification of any event, service or current website content. Confirm directly before travelling.

See [NETWORK.md](NETWORK.md) and the hub's release report for verification scope. Real service data should be added only with dated official evidence and explicit unknowns.
