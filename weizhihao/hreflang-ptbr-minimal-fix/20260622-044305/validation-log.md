# Weizhihao hreflang pt-BR Minimal Fix Validation

Validation time: 20260621T205502Z
Cache busting value: hreflang-ptbr-final-20260621T205502Z

## Scope
- Changed only frontend hreflang output for the existing `pt` language key when config html_lang is `pt-BR`.
- URL remains `/pt/`; key remains `pt`; html lang remains `pt-BR`; label remains `BR`; RU remains disabled; no WordPress page was saved or published.
- Cache actions performed after upload: LiteSpeed LSCache purge and Opcode Cache purge only.

## Diff
```diff
--- /Users/zhumulangmafeng/Documents/国外/records/hreflang-ptbr-minimal-fix/20260622-044305/wzh-seo-output-fixes.php.before	2026-06-22 04:43:13
+++ /Users/zhumulangmafeng/Documents/国外/records/hreflang-ptbr-minimal-fix/20260622-044305/wzh-seo-output-fixes.php.after	2026-06-22 04:44:56
@@ -279,7 +279,18 @@
 
     return isset($config[$lang]['html_lang']) ? $config[$lang]['html_lang'] : '';
 }
+
+function wzh_seo_output_plugin_i18n_hreflang_code($lang) {
+    $lang = sanitize_key((string) $lang);
+    $html_lang = wzh_seo_output_plugin_i18n_language_html_lang($lang);
+
+    if ($lang === 'pt' && strcasecmp($html_lang, 'pt-BR') === 0) {
+        return 'pt-BR';
+    }
 
+    return $lang;
+}
+
 function wzh_seo_output_plugin_i18n_language_is_enabled($lang) {
     $config = wzh_seo_output_plugin_i18n_language_config();
     $lang = sanitize_key((string) $lang);
@@ -1570,7 +1581,7 @@
     foreach ($group['languages'] as $lang => $url) {
         printf(
             '<link rel="alternate" hreflang="%s" href="%s" />' . "\n",
-            esc_attr($lang),
+            esc_attr(wzh_seo_output_plugin_i18n_hreflang_code($lang)),
             esc_url(wzh_seo_output_plugin_i18n_normalize_url($url))
         );
     }
@@ -1652,7 +1663,7 @@
             foreach ($alternates as $alt_lang => $alt_url) {
                 printf(
                     '    <xhtml:link rel="alternate" hreflang="%s" href="%s" />' . "\n",
-                    esc_attr($alt_lang),
+                    esc_attr(wzh_seo_output_plugin_i18n_hreflang_code($alt_lang)),
                     esc_url($alt_url)
                 );
             }
@@ -1712,7 +1723,7 @@
         $html .= sprintf(
             '<a class="wzh-i18n-header-entry__item" href="%s" hreflang="%s" lang="%s">%s</a>',
             esc_url(wzh_seo_output_plugin_i18n_normalize_url($url)),
-            esc_attr($lang),
+            esc_attr(wzh_seo_output_plugin_i18n_hreflang_code($lang)),
             esc_attr($lang),
             esc_html($label)
         );
```

## Page Validation

### https://weizhihaomachinery.com/
- Validation URL: https://weizhihaomachinery.com/?v=hreflang-ptbr-final-20260621T205502Z
- HTTP status: 200
- html lang: en-US
- canonical: https://weizhihaomachinery.com/
- canonical self: true
- hreflang codes: en / es / pt-BR / x-default
- exact hreflang="pt" count: 0
- contains pt-BR: true
- contains RU: false
- noindex: false
- x-litespeed-cache: miss
- cf-cache-status: DYNAMIC
- pass: true
- screenshot: home.png

### https://weizhihaomachinery.com/es/
- Validation URL: https://weizhihaomachinery.com/es/?v=hreflang-ptbr-final-20260621T205502Z
- HTTP status: 200
- html lang: es-ES
- canonical: https://weizhihaomachinery.com/es/
- canonical self: true
- hreflang codes: en / es / pt-BR / x-default
- exact hreflang="pt" count: 0
- contains pt-BR: true
- contains RU: false
- noindex: false
- x-litespeed-cache: miss
- cf-cache-status: DYNAMIC
- pass: true
- screenshot: es-home.png

### https://weizhihaomachinery.com/pt/
- Validation URL: https://weizhihaomachinery.com/pt/?v=hreflang-ptbr-final-20260621T205502Z
- HTTP status: 200
- html lang: pt-BR
- canonical: https://weizhihaomachinery.com/pt/
- canonical self: true
- hreflang codes: en / es / pt-BR / x-default
- exact hreflang="pt" count: 0
- contains pt-BR: true
- contains RU: false
- noindex: false
- x-litespeed-cache: miss
- cf-cache-status: DYNAMIC
- pass: true
- screenshot: pt-home.png

### https://weizhihaomachinery.com/es/producto/mf2510-2515cnc-rectificadora-lineal-automatica/
- Validation URL: https://weizhihaomachinery.com/es/producto/mf2510-2515cnc-rectificadora-lineal-automatica/?v=hreflang-ptbr-final-20260621T205502Z
- HTTP status: 200
- html lang: es-ES
- canonical: https://weizhihaomachinery.com/es/producto/mf2510-2515cnc-rectificadora-lineal-automatica/
- canonical self: true
- hreflang codes: en / es / pt-BR / x-default
- exact hreflang="pt" count: 0
- contains pt-BR: true
- contains RU: false
- noindex: false
- x-litespeed-cache: miss
- cf-cache-status: DYNAMIC
- pass: true
- screenshot: es-mf2510.png

### https://weizhihaomachinery.com/pt/produto/mf2510-2515cnc-retificadora-linear-automatica/
- Validation URL: https://weizhihaomachinery.com/pt/produto/mf2510-2515cnc-retificadora-linear-automatica/?v=hreflang-ptbr-final-20260621T205502Z
- HTTP status: 200
- html lang: pt-BR
- canonical: https://weizhihaomachinery.com/pt/produto/mf2510-2515cnc-retificadora-linear-automatica/
- canonical self: true
- hreflang codes: en / es / pt-BR / x-default
- exact hreflang="pt" count: 0
- contains pt-BR: true
- contains RU: false
- noindex: false
- x-litespeed-cache: miss
- cf-cache-status: DYNAMIC
- pass: true
- screenshot: pt-mf2510.png

### https://weizhihaomachinery.com/product/fully-automatic-circular-saw-blade-sharpening-machine-mf158cnc/
- Validation URL: https://weizhihaomachinery.com/product/fully-automatic-circular-saw-blade-sharpening-machine-mf158cnc/?v=hreflang-ptbr-final-20260621T205502Z
- HTTP status: 200
- html lang: en-US
- canonical: https://weizhihaomachinery.com/product/fully-automatic-circular-saw-blade-sharpening-machine-mf158cnc/
- canonical self: true
- hreflang codes: en / es / pt-BR / x-default
- exact hreflang="pt" count: 0
- contains pt-BR: true
- contains RU: false
- noindex: false
- x-litespeed-cache: miss
- cf-cache-status: DYNAMIC
- pass: true
- screenshot: en-mf158cnc.png

## JSON Check
- URL: https://weizhihaomachinery.com/wp-content/plugins/wzh-seo-output-fixes/config/i18n-settings.json?v=hreflang-ptbr-final-20260621T205502Z
- Status: 200
- pt.label: BR
- pt.html_lang: pt-BR
- pt.enabled: true
- ru.enabled: false

## Conclusion
- All pages passed: true
- Frontend hreflang now uses `pt-BR` for BR URLs and no exact `hreflang="pt"` remains in the checked pages.
- RU was not enabled and did not appear in checked hreflang output.