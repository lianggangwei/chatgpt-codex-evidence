# WZH Multilingual Content Pipeline and Core Page Matrix

Generated: 2026-06-22T15:32:35Z

Scope: read-only design and matrix build. No WordPress save, no publish, no registry edit, no cache purge, no RU enablement.

## Source of Truth Used

- Public registry: `i18n-registry.json` (12 groups)
- Public language settings: `i18n-settings.json`
- Public product directory: `i18n-product-directory.json`
- Public sitemaps: sitemap index, page, product, product category, post sitemap

Current language state from public settings:

- EN: enabled, `html_lang=en-US`
- ES: enabled, `html_lang=es-ES`
- BR: enabled as key `pt`, label `BR`, `html_lang=pt-BR`
- RU: present in config but disabled; not in the current processing phase

## 1. Current Site Page Type Classification

### Product Pages
Individual machine pages such as MF158CNC, MF2510CNC/MF2515CNC, MF223C, MF256, MF2718 series, MF250CNC, MF158C/MF158/MF128.

### Product Category Pages
Five commercial category entrances: saw blade grinder, straight knife grinder, universal tool grinder, blade grinding machine, profiling knife sharpening machine.

### FAQ
FAQ landing pages and deep FAQ posts. The current strategic model should use localized FAQ landing pages first, not copy all 298 FAQ entries at once.

### Articles / News
Technical articles, country/application notes, buyer guides, and lower-priority news posts. These should not be blanket-translated until products/categories and core trust pages are stable.

### About / Contact / Resources
Trust and conversion pages: About, Contact, Products hub, Resources/News index, and future localized resources landing pages.

## 2. Multilingual Processing Rules by Page Type

| Page type | ES needed | BR needed | RU needed now | Auto draft allowed | Human confirmation required | Rule |
|---|---:|---:|---:|---:|---:|---|
| Product pages | Yes for core/commercial models | Yes for core/commercial models | No | Yes | Yes | Generate ES/BR drafts from EN product page + glossary; publish only after preview QA and parent/slug confirmation. |
| Product category pages | Yes | Yes | No | Yes | Yes | Category pages are acquisition entrances; keep layout consistent with EN and validate WhatsApp/product links. |
| FAQ | Yes for landing/core questions | Yes for landing/core questions | No | Yes | Yes | Create localized FAQ landing pages first; registry only after publish and live validation. |
| Articles/news | Selective | Selective | No | Yes | Yes | Translate only evergreen buyer-intent posts or market-specific guides; skip broad news backlog initially. |
| About / Contact / Resources | Yes | Yes | No | Yes | Yes | Trust/contact wording needs manual QA; Contact and WhatsApp CTAs must be checked. |

## 3. Existing Core Page Matrix

Full CSV: `core-page-matrix.csv`.

### Registry-connected rows

| Page | EN | ES | BR | Status | Missing | Priority |
|---|---|---|---|---|---|---|
| Home | / (200) | /es/ (200) | /pt/ (200) | complete_in_registry | - | P0 |
| About | /about-us/ (200) | /es/sobre-nosotros/ (200) | /pt/sobre-nos/ (200) | complete_in_registry | - | P0 |
| Contact | /contact/ (200) | /es/contacto/ (200) | /pt/contato/ (200) | complete_in_registry | - | P0 |
| Products | /products/ (200) | /es/productos/ (200) | /pt/produtos/ (200) | complete_in_registry | - | P0 |
| Straight Knife Grinder | /product-category/straight-knife-grinder/ (200) | /es/afiladora-cuchillas-rectas/ (200) | /pt/afiadora-facas-retas/ (200) | complete_in_registry | - | P0 |
| Saw Blade Grinder | /product-category/saw-blade-grinder/ (200) | /es/afiladora-hojas-sierra/ (200) | /pt/afiadora-serra-circular/ (200) | complete_in_registry | - | P0 |
| Universal Tool Grinder | /product-category/universal-tool-grinder/ (200) | /es/afiladora-universal-herramientas/ (200) | /pt/afiadora-universal-ferramentas/ (200) | complete_in_registry | - | P0 |
| Blade Grinding Machine | /product-category/blade-grinding-machine/ (200) | /es/rectificadora-cuchillas-industriales/ (200) | /pt/retificadora-facas-industriais/ (200) | complete_in_registry | - | P0 |
| Profiling Knife Sharpening | /product-category/profiling-knife-sharpening-machine/ (200) | /es/afiladora-cuchillas-perfiladas/ (200) | /pt/afiadora-facas-perfiladas/ (200) | complete_in_registry | - | P0 |
| Mf158Cnc | /product/fully-automatic-circular-saw-blade-sharpening-machine-mf158cnc/ (200) | /es/producto/mf158cnc-afiladora-sierra-circular-cnc/ (200) | /pt/produto/mf158cnc-afiadora-serra-circular-cnc/ (200) | complete_in_registry | - | P0 |
| Mf2510 2515Cnc | /product/fully-automatic-linear-grinding-machine-mf2510cnc-mf2515cnc/ (200) | /es/producto/mf2510-2515cnc-rectificadora-lineal-automatica/ (200) | /pt/produto/mf2510-2515cnc-retificadora-linear-automatica/ (200) | complete_in_registry | - | P0 |
| FAQ | /faq/ (200) | /es/preguntas-frecuentes/ (200) | /pt/perguntas-frequentes/ (200) | complete_in_registry | - | P0 |

### Core gaps and planned rows

| Page | EN | ES | BR | Status | Missing | Priority |
|---|---|---|---|---|---|---|
| MF158C | /product/fully-automatic-circular-saw-blade-sharpening-machine-mf158c/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P2 |
| MF158 | /product/circular-saw-blade-grinding-machine-mf158/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P2 |
| MF128 | /product/circular-saw-blade-gear-grinding-machine-mf128/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P2 |
| MF2510C/2515C | /product/automatic-straight-knife-grinder-mf2510c-2515c/ (404) | - () | - () | not_in_registry_en_only | ES, BR | P2 |
| MF2718C-III | /product/universal-knife-sharpening-machine/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P1 |
| MF250CNC | /product/blade-sharpener-mf250cnc/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P1 |
| MF223C | /product/profiling-knife-sharpening-machine/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P1 |
| MF256 | /product/casting-automatic-linear-sharpener-mf256/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P1 |
| MF2718D | /product/mf2718d-universal-knife-sharpening-machine/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P1 |
| MF2718B-I | /product/mf2718b-i-universal-knife-sharpening-machine/ (200) | - () | - () | not_in_registry_en_only | ES, BR | P1 |
| News / Technical Articles index | /news/ (200) | - () | - () | not_in_registry | ES, BR | P1 |

## 4. Future Content Automation Flow

### New English Product Page

1. URL Matrix Scanner detects a new EN product URL from product sitemap, WooCommerce product list, or product directory.
2. Classifier assigns product family, commercial priority, and target locale requirements.
3. Translation Draft Generator creates ES and BR drafts using machine glossary, model specs, CTA rules, and localized buyer terminology.
4. WordPress Draft Creator creates draft pages only, with correct parent and slug; it does not publish.
5. Preview QA checks title, H1, CTA, product links, no garbled text, and no layout collapse.
6. Human publish approval is required.
7. Registry Updater adds EN/ES/BR group only after public pages return 200 and canonical self-check passes.
8. Hreflang Validator confirms `en`, `es`, `pt-BR`, and `x-default` full mesh.
9. Evidence Uploader commits logs, screenshots, CSV row update, and manifest to GitHub evidence.

### New News / Article Page

1. Classify topic: evergreen buyer guide, product selection, market-specific guide, temporary news, duplicate FAQ, or low-value update.
2. Translate only P0/P1 articles: product selection, buyer-intent, high-search-market, or sales-support content.
3. P2/P3 article backlog remains EN-only until Search Console/Bing data or buyer usage supports localization.
4. Localized article drafts must include canonical localization, not machine-only literal translation.
5. Registry entry only after publish and validation; do not bulk-register article URLs before pages exist.

### New FAQ Page

1. EN FAQ update enters FAQ queue.
2. If it belongs to core pre-sales selection, add summary answer to localized FAQ landing first.
3. If it is a deep technical FAQ, create ES/BR draft only when tied to high-priority product/category.
4. After publish, add FAQ group to registry and validate html lang/canonical/hreflang.

## 5. Automation Module Design

### URL Matrix Scanner

Reads public registry, i18n settings, product directory, sitemaps, and optional WordPress REST lists. Outputs a normalized matrix with page type, EN/ES/BR URLs, HTTP status, registry presence, and missing languages.

### Translation Draft Generator

Inputs EN source HTML/content, glossary, product specs, market tone, and CTA rules. Outputs localized page title, slug, meta description, body blocks, FAQ snippets, and internal link map. It must mark all output as draft-ready, not publish-ready.

### WordPress Draft Creator

Creates drafts with status `draft`, expected parent, stable slug, and metadata notes. It must fail closed if parent cannot be found. It never publishes and never edits the EN source.

### Preview QA

Checks preview/public draft for title, language naturalness, CTA links, WhatsApp/contact/category links, no shortcode leakage, no empty content, no 404/redirect surprises, and no layout collapse.

### Registry Updater

Runs only after pages are published and validated. Backs up registry, adds one page group at a time, uses BR key `pt` with `hreflang/html_lang=pt-BR`, and produces a diff before upload.

### Hreflang Validator

Checks each group for 200 status, self canonical, html lang, alternates `en/es/pt-BR/x-default`, reciprocal return tags, no `hreflang=pt`, no RU unless explicitly enabled later, and no noindex.

### Evidence Uploader

Writes report, CSV, logs, screenshots for anomalies, and manifest to GitHub evidence. Every batch has a timestamped folder and rollback notes.

## 6. Risk Controls

- Draft first: automated writing can create drafts only.
- No auto publish: publishing requires explicit user confirmation.
- No RU in current phase: RU can stay planned/disabled but must not enter switcher, registry, or hreflang now.
- GitHub evidence: every batch produces log, CSV, manifest, and screenshots for anomalies.
- Backups: registry/config updates require a remote backup path and a local diff.
- Rollback: registry rollback is restore previous JSON backup; page rollback is draft/unpublish or revert page revision; cache purge only when needed and documented.
- Parent/slug gate: localized pages must have correct parent and slug before publishing.
- Cache caution: validate with cache-busting URLs before deciding whether cache is stale.

## 7. Recommended Execution Order

### Batch First

1. Keep current P0 registry pages stable: Home, Products, five categories, About, Contact, FAQ, MF158CNC, MF2510/2515CNC.
2. Verify and complete core product ES/BR drafts for missing P1 products: MF223C, MF256, MF2718C-III/MF2718D/MF2718B-I, MF250CNC, MF158C/MF158/MF128.
3. Add localized Resources/News landing after product/category coverage is stable.
4. Batch localized FAQ additions only for high-value buying questions.

### Articles Not To Batch Now

- Country-specific low-signal posts with no Search Console/Bing evidence.
- Short maintenance/news updates that do not support product selection.
- Duplicate or near-duplicate FAQ-derived posts.
- Any article whose localized page would not naturally drive WhatsApp inquiry or product-category navigation.

### Pages To Batch

- Product categories: all five category pages should remain complete in ES/BR.
- Product pages: batch by product family, not one isolated page at a time.
- Trust/conversion pages: About, Contact, FAQ, Resources landing.

## Evidence Notes

No live site mutation was performed. HTTP statuses in the CSV come from read-only GET checks with a Codex audit user agent. Screenshots were not required because this stage is a pipeline and matrix design; key evidence is the public config snapshot, sitemap snapshot, CSV, and manifest.
