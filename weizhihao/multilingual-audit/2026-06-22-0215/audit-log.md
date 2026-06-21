# Weizhihao Multilingual Audit Evidence

Audit time: 2026-06-22 02:15:51 CST
Repository path: weizhihao/multilingual-audit/2026-06-22-0215
Mode: read-only validation. No WordPress page save, publish, code edit, or website configuration change was performed during this evidence pass.

## Evidence Items

### 1. MF2510CNC / MF2515CNC ES product page
- Page / position: MF2510CNC / MF2515CNC ES page
- URL: https://weizhihaomachinery.com/es/producto/mf2510-2515cnc-rectificadora-lineal-automatica/
- Language: es / html lang es-ES
- Status: normal
- Screenshot: es-mf2510.png
- Observed result: HTTP 200, Spanish title and H1 present, MF2510CNC / MF2515CNC content visible.

### 2. MF2510CNC / MF2515CNC PT product page
- Page / position: MF2510CNC / MF2515CNC PT page
- URL: https://weizhihaomachinery.com/pt/produto/mf2510-2515cnc-retificadora-linear-automatica/
- Language: pt / html lang pt-BR
- Status: normal with naming caveat
- Screenshot: pt-mf2510.png
- Observed result: HTTP 200, Portuguese title and H1 present, MF2510CNC / MF2515CNC content visible. The actual HTML language is pt-BR while the visible entry still uses PT naming.

### 3. PT / BR home entry state
- Page / position: PT/BR language entry on home-equivalent page
- URL: https://weizhihaomachinery.com/pt/
- Language: pt / html lang pt-BR
- Status: abnormal / naming mismatch
- Screenshot: pt-home-br-state.png
- Observed result: HTTP 200 and page language is pt-BR, but the frontend language selector still displays PT rather than BR.

### 4. RU home placeholder
- Page / position: RU entry page
- URL: https://weizhihaomachinery.com/ru/
- Language: ru
- Status: abnormal / reserved or not ready
- Screenshot: ru-home.png
- Observed result: HTTP 200 but page shows an update placeholder and sends noindex, nofollow. This is not a complete Russian rollout page.

### 5. RU MF2510CNC / MF2515CNC product route
- Page / position: RU MF2510CNC / MF2515CNC product page candidate
- URL: https://weizhihaomachinery.com/ru/produkt/mf2510-2515cnc-avtomaticheskii-lineinyi-stanok/
- Language: expected ru, actual fallback en-US 404
- Status: abnormal / not found
- Screenshot: ru-mf2510-404.png
- Observed result: HTTP 404 and Page not found. Russian product route is not live.

### 6. EN home language entry
- Page / position: homepage language selector
- URL: https://weizhihaomachinery.com/
- Language: en / html lang en-US
- Status: normal with missing BR/RU entry caveat
- Screenshot: en-home-language-entry.png
- Observed result: HTTP 200. Selector shows EN / ES / PT. No visible BR or RU entry was observed.

### 7. WordPress pages search for ES
- Page / position: WordPress backend pages search, ES
- URL: https://weizhihaomachinery.com/wp-admin/edit.php?post_type=page&s=es
- Language: backend / ES search
- Status: verified screenshot only
- Screenshot: wp-pages-es-search.png
- Observed result: WordPress admin page was accessible in the current logged-in session.

### 8. WordPress pages search for PT
- Page / position: WordPress backend pages search, PT
- URL: https://weizhihaomachinery.com/wp-admin/edit.php?post_type=page&s=pt
- Language: backend / PT search
- Status: verified screenshot only
- Screenshot: wp-pages-pt-search.png
- Observed result: WordPress admin page was accessible in the current logged-in session.

### 9. WordPress pages search for RU
- Page / position: WordPress backend pages search, RU
- URL: https://weizhihaomachinery.com/wp-admin/edit.php?post_type=page&s=ru
- Language: backend / RU search
- Status: verified screenshot only
- Screenshot: wp-pages-ru-search.png
- Observed result: WordPress admin page was accessible in the current logged-in session.

### 10. WordPress WPCode multilingual output snippet state
- Page / position: WPCode snippet 4823 current state
- URL: https://weizhihaomachinery.com/wp-admin/admin.php?page=wpcode-snippet-manager&snippet_id=4823
- Language: backend / configuration
- Status: verified screenshot only
- Screenshot: wpcode-4823-current.png
- Observed result: Current WPCode page was captured. Browser CDP screenshot timed out on this admin screen, so the screenshot was captured with the macOS screencapture fallback while the WPCode tab was visible. No save/publish was performed.

## Error / Exception Notes

- No live 403 page was observed during this evidence pass.
- No WordPress save was attempted during this evidence pass, so there is no new save-failure screen to capture.
- Browser CDP screenshot failed on the WPCode admin page with a screenshot timeout; macOS screencapture fallback was used for `wpcode-4823-current.png`.
- Earlier automation-side editor manipulation was not used as proof of a website change and did not result in a WordPress update action.

## Key Findings

- ES product page is live and visually reachable.
- PT product page is live, but the implementation is actually pt-BR at the HTML/config level.
- Frontend language selector still displays PT, not BR.
- RU is not production-ready: `/ru/` is a noindex placeholder, and the tested RU MF2510/MF2515 route is 404.
- Backend pages/admin screens are accessible in the current logged-in session, but this audit did not save or publish any changes.
