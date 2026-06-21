# Weizhihao i18n PT Label to BR Evidence

Audit time: 2026-06-22 03:05 CST
Mode: minimal live config change
GitHub evidence directory: weizhihao/i18n-label-br/2026-06-22-0305

## Scope

Requested change: only change the live `config/i18n-settings.json` language setting `languages.pt.label` from `PT` to `BR`.

Strictly not changed:
- URL structure remains `/pt/`
- Language key remains `pt`
- `html_lang` remains `pt-BR`
- `enabled` remains unchanged
- `ru` remains unchanged
- registry remains unchanged
- product directory remains unchanged
- `wzh-seo-output-fixes.php` remains unchanged
- WPCode remains unchanged
- no WordPress page was saved or published
- no plugin package was uploaded

## Backup and Upload

Initial wrong-root attempt:
- I first wrote to FTP root `/public_html/...`, which is not the active site root.
- This was detected by comparing the public JSON URL and the FTP path.
- The wrong-root file was restored to its original backup.
- Restore verification: `wrong_restored_match=True`.

Correct active site path:
- Remote path: `/domains/weizhihaomachinery.com/public_html/wp-content/plugins/wzh-seo-output-fixes/config/i18n-settings.json`
- Backup path: `/Users/zhumulangmafeng/Documents/国外/records/i18n-settings-label-br-2026-06-22/i18n-settings.domain-before.json`
- Uploaded verification path: `/Users/zhumulangmafeng/Documents/国外/records/i18n-settings-label-br-2026-06-22/i18n-settings.domain-after-upload.json`
- Upload verification: `correct_after_match=True`
- JSON validation: `domain remote after json valid`

## Diff

```diff
@@ -14,7 +14,7 @@
       "enabled": true
     },
     "pt": {
-      "label": "PT",
+      "label": "BR",
       "html_lang": "pt-BR",
       "dir": "ltr",
       "enabled": true
```

## Cache Actions

Used current WordPress admin session to purge only:
- LiteSpeed LSCache
- LiteSpeed Opcode Cache

No CSS/JS, UCSS, VPI, page save, or publish action was performed.

## HTTP Verification

### Home
- URL: https://weizhihaomachinery.com/
- Response evidence: `x-litespeed-cache: miss`, `cf-cache-status: DYNAMIC`
- HTML: `<html ... lang="en-US">`
- Language entry: `EN / ES / BR`
- Screenshot: `home-language-entry-br.png`

### PT home
- URL: https://weizhihaomachinery.com/pt/
- Response evidence: `x-litespeed-cache: miss`, `cf-cache-status: DYNAMIC`
- HTML: `<html ... lang="pt-BR">`
- Language entry: `EN / ES / BR`
- Screenshot: `pt-home-language-entry-br.png`

### PT MF2510CNC / MF2515CNC product page
- URL: https://weizhihaomachinery.com/pt/produto/mf2510-2515cnc-retificadora-linear-automatica/
- Response evidence: `x-litespeed-cache: miss`, `cf-cache-status: DYNAMIC`
- HTML: `<html ... lang="pt-BR">`
- Language entry: `EN / ES / BR`
- Screenshot: `pt-mf2510-language-entry-br.png`

### Public config URL
- URL: https://weizhihaomachinery.com/wp-content/plugins/wzh-seo-output-fixes/config/i18n-settings.json
- `last-modified: Sun, 21 Jun 2026 19:00:59 GMT`
- `pt.label=BR`
- `pt.html_lang=pt-BR`
- `pt.enabled=true`
- `ru.enabled=false`

## Screenshot URLs

- Home: https://raw.githubusercontent.com/lianggangwei/chatgpt-codex-evidence/main/weizhihao/i18n-label-br/2026-06-22-0305/home-language-entry-br.png
- PT home: https://raw.githubusercontent.com/lianggangwei/chatgpt-codex-evidence/main/weizhihao/i18n-label-br/2026-06-22-0305/pt-home-language-entry-br.png
- PT product: https://raw.githubusercontent.com/lianggangwei/chatgpt-codex-evidence/main/weizhihao/i18n-label-br/2026-06-22-0305/pt-mf2510-language-entry-br.png

## Conclusion

The requested minimal change is live on the active site root. EN / ES / BR now appears on home, `/pt/`, and the PT MF2510CNC / MF2515CNC product page. RU was not changed or added.
