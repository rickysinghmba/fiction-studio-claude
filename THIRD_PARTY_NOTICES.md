# Third-party notices

The craft plugins in this repository draw ideas from the
open-source projects below. They are released under the MIT licence. The wording of our rules
and checks is our own; no source code from these projects is included. Their notices are
reproduced here as the licence asks.

| Project | Copyright |
| --- | --- |
| sepia | Copyright (c) 2026 Nanako Tsai |
| book-writer-skill | Copyright (c) 2026 Shubhanshu Shukla |
| Fibb | Copyright (c) 2026 Writing Secrets, Beach Blogger LLC |
| NovelClaw | Copyright (c) iLearn-Lab |

Each plugin card in the studio names the projects it draws on.

## Other open-source code in the Writing Studio

| Project | Copyright | Used for |
| --- | --- | --- |
| streaming-markdown 0.2.15 (https://github.com/thetarnav/streaming-markdown) | Copyright (c) 2024 Damian Tarnawski | Formatting Claude's replies in the studio chat and Write's Claude panel as they stream (bundled in the site's scripts) |
| foliate-js (https://github.com/johnfactotum/foliate-js) | Copyright (c) 2022 John Factotum · MIT | "Preview as a reader" on the Format page (vendored unmodified in public/vendor/foliate-js) |
| zip.js (https://github.com/gildas-lormeau/zip.js) | Copyright (c) Gildas Lormeau · BSD-3-Clause | Opening the ebook inside the preview (minified build shipped with foliate-js) |
| satori (https://github.com/vercel/satori) | Copyright (c) Vercel, Inc. · MPL-2.0 | Drawing share cards for author, book and chapter pages (used unmodified; source at the link) |
| resvg-wasm (https://github.com/yisibl/resvg-js) | Copyright (c) the resvg-js authors · MPL-2.0 | Turning share cards into PNG images (used unmodified; source at the link) |
| uPlot 1.6.32 (https://github.com/leeoniya/uPlot) | Copyright (c) 2022 Leon Sorokin · MIT | Charts on the Analytics page (bundled in the site's scripts) |
| web-vitals 6.2.3 (https://github.com/GoogleChrome/web-vitals) | Copyright Google LLC · Apache-2.0 | Measuring page speed on readers' devices for author website analytics (bundled in the site's scripts, unmodified) |
| Umami (https://github.com/umami-software/umami) | Copyright (c) 2020 Mike Cao · MIT | Optional cookie-free visitor counts for the main site; its script is loaded from your own Umami, not shipped here |
| schema-dts (https://github.com/google/schema-dts) | Copyright Google LLC · Apache-2.0 | Type-checking the structured data on author, book and chapter pages (types only; nothing ships to browsers) |

The chat's "follow the newest text" scrolling follows the approach of use-stick-to-bottom by StackBlitz (MIT); the code is our own.

## MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software
and associated documentation files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or
substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING
BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
