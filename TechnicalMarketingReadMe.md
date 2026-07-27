# Technical Marketing Summary — biofool.github.io

## One-Line Positioning

A GitHub Pages site delivering a standards-based, multi-language QR Code generator alongside a vision for decentralized media provenance (Truthiness Discovery Network).

## Target Users / Personas

- **Web developers** who need a lightweight, dependency-free QR Code generation library they can embed directly in HTML.
- **Cross-platform engineers** who want reference QR Code implementations across JavaScript, TypeScript, Java, Python, PHP, Ruby, ActionScript 3, and Hack.
- **Media provenance advocates / researchers** interested in the concept of a public ledger for media truthiness and deep-fake detection.

## Key Features (Grounded in Code)

- **Multi-language QR Code generation** — implementations in 8 languages (`js/`, `ts/`, `java/`, `python/`, `php/`, `ruby/`, `as3/`, `hack/`), all based on JIS X 0510:1999.
- **JavaScript API** — `qrcode(typeNumber, errorCorrectionLevel)` with `addData()`, `make()`, and multiple render helpers: `createImgTag()`, `createSvgTag()`, `createTableTag()`, `createDataURL()`, `createASCII()`, `renderTo2dContext()`.
- **Configurable error correction** — levels L, M, Q, H; type numbers 1–40 (or 0 for auto-detection).
- **Live demo** — published via GitHub Pages at `https://biofool.github.io/qrcode/js/demo/`.
- **Mocha test suite** — included for the JavaScript implementation (`qrcode/js/test/`).
- **Truthiness Discovery Network concept** — a landing/vision page for decentralized, public media provenance to combat deep fakes and fake news.

## Technical Differentiators

- **Standards-compliant** — built directly on the JIS X 0510:1999 QR Code specification.
- **Zero-dependency JavaScript** — `qrcode.js` is a single self-contained file; no build step required for basic usage.
- **Polyglot reference set** — rare to find the same algorithm ported across 8 languages in one repo, enabling cross-language consistency and learning.
- **Multiple output formats** — image tag, SVG, HTML table, data URL, ASCII art, and direct canvas/2D-context rendering.

## Use Cases

- Embedding QR codes in web pages without a third-party service or API calls.
- Generating QR codes server-side in Java, Python, PHP, or Ruby environments.
- Educational reference for how QR Code encoding works across languages.
- Exploring the concept of a public media-provenance ledger.

## Benefits / Value Proposition

- **No external API dependency** — QR codes generated entirely client-side or in-process, reducing latency and cost.
- **Broad language coverage** — pick the port that fits your stack; consistent behavior across implementations.
- **Free and open** — MIT-licensed, hosted on GitHub Pages with a live demo.
- **Flexible rendering** — choose the output format that best fits your application (raster image, vector SVG, ASCII, or canvas).

## Tech Stack

- **Languages**: JavaScript, TypeScript, Java (Gradle), Python, PHP, Ruby, ActionScript 3, Hack (HHVM)
- **Testing**: Mocha (JavaScript)
- **Hosting**: GitHub Pages
- **License**: MIT

## Known Limitations

- The Truthiness Discovery Network is a concept/vision page only; no backing ledger, API, or service code is included in this repository.
- The QR Code implementations are based on the 1999 JIS standard and may not include newer QR Code 2005 features.
- No bundled npm package is published from this repo (the upstream `qrcode-generator` npm package is maintained separately by the original author).
- ActionScript 3 and Hack ports target legacy/niche runtimes (Flash/HHVM).
