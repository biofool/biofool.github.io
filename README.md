# biofool.github.io

GitHub Pages site for user `biofool`, hosting a multi-language **QR Code Generator** and the **Truthiness Discovery Network (TDN)** concept page.

## Overview

This repository powers the GitHub Pages site at `https://biofool.github.io/`. It contains two main things:

1. **QR Code Generator** (`qrcode/`) — a multi-language QR Code generation library (JavaScript, TypeScript, Java, Python, PHP, Ruby, ActionScript 3, Hack) based on the JIS X 0510:1999 standard. A live JavaScript demo is published via GitHub Pages.
2. **Truthiness Discovery Network (TDN)** — a concept/landing page describing a vision for decentralized, public media provenance to combat deep fakes and fake news.

## Prerequisites

- A modern web browser to view the Pages site and demos.
- For local development of the JavaScript library: [Node.js](https://nodejs.org/) and `npm` (to run tests with Mocha).
- For the other language ports: the respective language toolchains (JDK for Java, Python 3, PHP, Ruby, etc.) — only needed if you want to build/run those ports.

## Setup

```bash
git clone https://github.com/biofool/biofool.github.io.git
cd biofool.github.io
```

Open `qrcode/js/sample.html` in a browser, or visit the live demo:
<https://biofool.github.io/qrcode/js/demo/>

### Running the JavaScript tests

```bash
cd qrcode/js
npm install
npm test
```

## How to Use the QR Code Generator (JavaScript)

1. Include `qrcode.js` in your HTML.
2. Add a placeholder element.
3. Generate the QR code and render it.

```html
<script type="text/javascript" src="qrcode.js"></script>
<div id="placeHolder"></div>
<script>
  var qr = qrcode(4, 'L');      // typeNumber 1-40 (0 = auto), errorCorrectionLevel 'L'|'M'|'Q'|'H'
  qr.addData('Hi!');
  qr.make();
  document.getElementById('placeHolder').innerHTML = qr.createImgTag();
</script>
```

Output helpers: `createImgTag()`, `createSvgTag()`, `createTableTag()`, `createDataURL()`, `createASCII()`, and `renderTo2dContext()`.

## Project Structure

```
biofool.github.io/
├── README.md                 # This file
├── qrcode/                   # QR Code Generator (multi-language)
│   ├── js/                   # JavaScript implementation + demo + tests
│   ├── ts/                   # TypeScript port
│   ├── java/                 # Java port (Gradle project)
│   ├── python/               # Python port
│   ├── php/                  # PHP port + samples
│   ├── ruby/                 # Ruby port
│   ├── as3/                  # ActionScript 3 port
│   ├── hack/                 # Hack (HHVM) port
│   └── LICENSE               # MIT
└── (GitHub Pages content for the TDN concept)
```

## Notes

- "QR Code" is a registered trademark of DENSO WAVE INCORPORATED.
- The QR Code implementations are based on JIS X 0510:1999 and licensed under the MIT License.
- The Truthiness Discovery Network is a concept/vision page; no backing service code is included in this repository.
