# FAQ i18n registry minimal integration

- Time UTC: 2026-06-22T06:02:23Z
- Changed file: `wp-content/plugins/wzh-seo-output-fixes/config/i18n-registry.json`
- Change scope: added only the `faq` registry group for EN / ES / BR.
- Cache clearing: not performed; formal URLs reflected the registry change immediately.
- RU: not added to FAQ group and not enabled through this change.

## URLs verified
### EN FAQ
- URL: https://weizhihaomachinery.com/faq/
- HTTP: 200
- html lang: `en-US`
- canonical: `https://weizhihaomachinery.com/faq/`
- hreflang: `en, es, pt-BR, x-default`
- language entry: `EN ES BR EN ES BR`
- hreflang=pt present: `False`
- RU present: `False`

### ES FAQ
- URL: https://weizhihaomachinery.com/es/preguntas-frecuentes/
- HTTP: 200
- html lang: `es-ES`
- canonical: `https://weizhihaomachinery.com/es/preguntas-frecuentes/`
- hreflang: `en, es, pt-BR, x-default`
- language entry: `EN ES BR EN ES BR`
- hreflang=pt present: `False`
- RU present: `False`

### BR FAQ
- URL: https://weizhihaomachinery.com/pt/perguntas-frequentes/
- HTTP: 200
- html lang: `pt-BR`
- canonical: `https://weizhihaomachinery.com/pt/perguntas-frequentes/`
- hreflang: `en, es, pt-BR, x-default`
- language entry: `EN ES BR EN ES BR`
- hreflang=pt present: `False`
- RU present: `False`

## Evidence
- Diff: https://github.com/lianggangwei/chatgpt-codex-evidence/blob/main/weizhihao/faq-i18n-registry/20260622T060223Z/diff-i18n-registry-faq-only.diff
- Manifest: https://github.com/lianggangwei/chatgpt-codex-evidence/blob/main/weizhihao/faq-i18n-registry/20260622T060223Z/manifest.json
- Validation JSON: https://github.com/lianggangwei/chatgpt-codex-evidence/blob/main/weizhihao/faq-i18n-registry/20260622T060223Z/validation.json
- EN screenshot: https://github.com/lianggangwei/chatgpt-codex-evidence/blob/main/weizhihao/faq-i18n-registry/20260622T060223Z/en-faq.png
- ES screenshot: https://github.com/lianggangwei/chatgpt-codex-evidence/blob/main/weizhihao/faq-i18n-registry/20260622T060223Z/es-faq.png
- BR screenshot: https://github.com/lianggangwei/chatgpt-codex-evidence/blob/main/weizhihao/faq-i18n-registry/20260622T060223Z/br-faq.png
