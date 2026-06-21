# Weizhihao FAQ ES / BR Preparation Report

Audit time: 20260621T212817Z
Mode: read-only. No website changes, no WordPress saves, no publish, no plugin/config edits, no cache purge, no RU work.

## EN FAQ
- URL: https://weizhihaomachinery.com/faq/
- Page ID: 4195
- Page title: Sharpening Machine FAQ
- Browser title: Sharpening Machine FAQ | Buying, Shipping and Customization
- Status: publish
- html lang: en-US
- Canonical: https://weizhihaomachinery.com/faq/
- Rendered content bytes: 212749
- Extracted H2 questions: 298

## ES / BR Existence
- EN FAQ: requested https://weizhihaomachinery.com/faq/; status 200; final https://weizhihaomachinery.com/faq/; history []
- ES /es/faq/: requested https://weizhihaomachinery.com/es/faq/; status 200; final https://weizhihaomachinery.com/faq/; history [{'status': 301, 'location': 'https://weizhihaomachinery.com/faq/'}]
- BR /pt/faq/: requested https://weizhihaomachinery.com/pt/faq/; status 200; final https://weizhihaomachinery.com/faq/; history [{'status': 301, 'location': 'https://weizhihaomachinery.com/faq/'}]
- Suggested ES: requested https://weizhihaomachinery.com/es/preguntas-frecuentes/; status 404; final https://weizhihaomachinery.com/es/preguntas-frecuentes/; history []
- Suggested BR: requested https://weizhihaomachinery.com/pt/perguntas-frequentes/; status 404; final https://weizhihaomachinery.com/pt/perguntas-frequentes/; history []

## Recommended URLs
- ES: https://weizhihaomachinery.com/es/preguntas-frecuentes/
- BR: https://weizhihaomachinery.com/pt/perguntas-frequentes/

## Current EN Content Structure
- Intro blocks: 1
  - Below are the most common questions buyers ask before choosing a sharpening machine from WEIZHIHAO.
- H2 question count: 298
- First 20 questions:
  1. How do I choose the right sharpening machine?
  2. What types of sharpening machines do you offer?
  3. Do your machines come with a warranty?
  4. Can you provide custom sharpening solutions?
  5. Which industries use your sharpening machines?
  6. Do you ship sharpening machines internationally?
  7. How do I assess a supplier's technical capability for grinding machines?
  8. What quality control measures indicate a reliable Chinese grinding machine supplier?
  9. What key details should be included in a transparent quotation for grinding machines?
  10. What after-sales support aspects are critical when sourcing grinding machines from China?
  11. How can I verify a supplier's reputation and reliability through references?
  12. What safety details should buyers check before ordering an industrial knife grinder?
  13. How can factories confirm grinding accuracy before purchase?
  14. Which production details help match an industrial knife grinder correctly?
  15. Why should a buyer compare maintenance access when choosing a knife grinder?
  16. What core specifications should I request before asking for a quote?
  17. How can I assess a supplier’s quality control and machine consistency?
  18. What long-term costs should I consider apart from the purchase price?
  19. What technical support and training come with the machine?
  20. How do I verify a supplier’s export experience and regulatory compliance?
- Section title candidates: Evaluating Chinese Grinding Machine Suppliers, Industrial Knife Grinder Questions, Industrial Grinder Procurement FAQ, Sharpening Machine Buyer Questions, Straight Knife Grinder Uptime, Coolant Filtration for Knife Grinding Machines, Pre-FAT Installation Verification, Spare Parts Planning for Importers, Operator Training for Straight Knife Grinder Accuracy, Coolant and Wheel Care Procurement Notes, Pre-Shipment Documentation, Factory Acceptance Photo Records, Sharpening Machine Handoff Checklist, Commissioning Essentials, Saw Blade Grinder Questions, Shipping Sharpening Machines, Insert Grinder Buying Checklist FAQs, Profile Knife Grinder Questions, Wood Chipper Knife Grinder Selection, Straight Knife Grinder Buying & Maintenance

## Draft Files
- ES draft: es-faq-draft.md
- BR draft: br-faq-draft.md
- Full EN question backlog: en-faq-question-backlog.md

## Minimal Safe Plan
1. Create ES FAQ as a draft page at /es/preguntas-frecuentes/ using the ES draft, without publishing until preview is verified.
2. Create BR FAQ as a draft page at /pt/perguntas-frequentes/ using the BR draft, without publishing until preview is verified.
3. After both drafts are approved, publish and then add the FAQ group to the i18n hreflang registry so EN/ES/BR mutually link.
4. Keep /pt/ as the BR URL prefix and keep html lang pt-BR; do not touch RU.
5. Later translate child FAQ detail pages in batches; do not try to translate all 298 FAQ items in one risky live edit.

## Risks
- /es/faq/ and /pt/faq/ currently 301 to the EN /faq/ page, so those paths should not be reused without checking rewrite behavior.
- The EN FAQ page is very large (298 H2 questions); translating the entire page in one backend edit is high risk for quality and timeout.
- New ES/BR FAQ pages will not provide SEO hreflang value until they are published and mapped into the hreflang registry.
- Partial translation should be clearly structured as a localized FAQ landing page; detailed child FAQ pages should be translated later in controlled batches.