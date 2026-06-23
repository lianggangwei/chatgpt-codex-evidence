# Weizhihao P1 Product i18n publish and registry evidence

Created: 2026-06-23T17:43:05Z

Scope:
- Published ES/BR pages for product-mf223c, product-mf2718c-iii, product-mf256.
- Added only these three groups to live i18n registry.
- RU not enabled or added.

Key validation:
- Public registry contains product-mf223c, product-mf2718c-iii, product-mf256.
- 9 URLs checked: EN/ES/BR for three product groups.
- All returned 200.
- html lang matched en-US / es-ES / pt-BR.
- canonical self checks passed.
- hreflang set is en / es / pt-BR / x-default.
- No hreflang="pt" and no RU detected.
- Visual screenshots confirm EN/ES/BR language entry on MF223C pages.

Important path finding:
- Initial upload to FTP /public_html was not the live docroot.
- Real live docroot is /domains/weizhihaomachinery.com/public_html/.
- Live registry backup and upload report are included.
