# ⚡ QuickTools

A fast, free suite of browser-based tools, hosted on GitHub Pages:
**https://a-haz.github.io/test/**

Every tool is a single static HTML page — no backend, no build step, no
frameworks, no trackers. All processing happens client-side, so user data
never leaves the browser.

## Tools

| Tool | Path | Search intent |
|---|---|---|
| 🧾 Invoice Generator | `/invoice-generator/` | "free invoice generator" — high commercial intent |
| 🖼️ Image Compressor & Resizer | `/image-compressor/` | "compress image" — huge volume; privacy angle is the differentiator |
| 📱 QR Code Generator | `/qr-code-generator/` | "qr code generator free" — huge volume; "never expires" is the hook |
| 🏦 Loan Calculator | `/loan-calculator/` | "loan calculator" — finance niche, top-tier ad CPC |
| ⚖️ BMI Calculator | `/bmi-calculator/` | "bmi calculator" — health niche, high volume + CPC |
| 💰 Salary Converter | `/salary-converter/` | "hourly to salary" — finance niche |
| 🪄 JSON Formatter & Validator | `/json-formatter/` | "json formatter", "json validator" |
| 🔐 Password Generator | `/password-generator/` | "password generator" |
| 📝 Word Counter | `/word-counter/` | "word counter", "character count" |
| 🔁 Base64 Encode/Decode | `/base64/` | "base64 decode" |
| 📊 Percentage Calculator | `/percentage-calculator/` | "percentage calculator" |
| ⏱ Timestamp Converter | `/timestamp-converter/` | "unix timestamp converter", "epoch converter" |
| 🔤 Case Converter | `/case-converter/` | "case converter", "title case converter" |

The QR tool bundles the MIT-licensed
[qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator)
library (vendored at `qr-code-generator/qrcode.js`); everything else is
hand-written vanilla JS.

Plus: `privacy.html`, `404.html`, `sitemap.xml`, `robots.txt`.

## How to monetize this site

1. **Get traffic first.** Submit the sitemap in [Google Search Console](https://search.google.com/search-console)
   and Bing Webmaster Tools. Share individual tools where they're useful
   (the invoice generator in freelancer communities, the JSON formatter in dev
   threads). Rankings for tool keywords take months — patience required.
2. **Buy a custom domain (~$10/yr) before applying for ads.**
   Google AdSense does **not** accept `*.github.io` subdomains — you must
   serve the site from a domain you own. Point it at GitHub Pages
   (Settings → Pages → Custom domain), update the `canonical` URLs,
   `sitemap.xml` and `robots.txt`, then apply.
3. **Add the ad units.** Each tool page contains an
   `<!-- AdSense: paste a responsive ad unit here once approved -->` comment
   marking a sensible placement. Update `privacy.html` when ads go live —
   AdSense requires the policy to disclose it.
4. **Alternatives that work without AdSense:** [EthicalAds](https://www.ethicalads.io/)
   or [Carbon Ads](https://www.carbonads.net/) for dev-audience pages,
   affiliate links (e.g. accounting/invoicing software on the invoice page,
   password managers on the password page), or a "Buy me a coffee" link.

## Adding a new tool

Copy any tool folder (e.g. `word-counter/`), keep the header/footer markup,
write the tool UI + inline script, give it a unique `<title>`,
`meta description` and `canonical` URL, then add it to `index.html`,
the footer lists and `sitemap.xml`.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

No build step needed — it's plain HTML/CSS/JS.
