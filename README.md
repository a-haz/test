# QuickTools

A set of small browser tools, hosted on GitHub Pages at
https://a-haz.github.io/test/

Each tool is one static HTML page with inline JavaScript and a shared
`style.css`. There is no backend and no build step, and input is processed in
the browser, not sent to a server.

## Tools

| Tool | Path |
|---|---|
| Invoice generator (print or save as PDF) | `/invoice-generator/` |
| Image compressor and resizer | `/image-compressor/` |
| QR code generator | `/qr-code-generator/` |
| Loan calculator with amortization table | `/loan-calculator/` |
| BMI calculator | `/bmi-calculator/` |
| Salary converter (hourly, monthly, yearly) | `/salary-converter/` |
| Compound interest calculator | `/compound-interest-calculator/` |
| Discount and tip calculator | `/discount-calculator/` |
| Unit converter | `/unit-converter/` |
| Age calculator | `/age-calculator/` |
| JSON formatter and validator | `/json-formatter/` |
| Password generator | `/password-generator/` |
| Hash generator (SHA-1, SHA-256, SHA-384, SHA-512) | `/hash-generator/` |
| Text diff | `/text-diff/` |
| Word counter | `/word-counter/` |
| Base64 encode and decode | `/base64/` |
| Percentage calculator | `/percentage-calculator/` |
| Unix timestamp converter | `/timestamp-converter/` |
| Case converter | `/case-converter/` |

There are also two short guides under `/guides/` (writing an invoice,
compressing images for email), plus `privacy.html`, `404.html`, `sitemap.xml`
and `robots.txt`.

## Notes

- The QR tool uses the MIT-licensed
  [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) library,
  vendored at `qr-code-generator/qrcode.js`. Everything else is plain
  JavaScript.
- Hashing uses the browser's Web Crypto API, which only supports the SHA family,
  so there is no MD5.
- The password generator uses `crypto.getRandomValues()`.
- Tool pages have an HTML comment marking where an ad unit could go. No ads are
  running.

## Adding a tool

Copy an existing tool folder (for example `word-counter/`), keep the header and
footer markup, write the page and its script, set a unique `<title>`, meta
description and canonical URL, then add it to `index.html`, the footer link
lists and `sitemap.xml`.

## Running locally

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```
