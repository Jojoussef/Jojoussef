# Youssef Benatti

Software engineer in Monastir, Tunisia. Most of my day goes into Python backends, Go network clients, and TypeScript web applications, with a particular habit of chasing down parser and state-sync bugs in upstream open-source libraries when I hit them in my own work.

### Upstream Open-Source Patches

Merged pull requests in third-party repositories:

- **[go-resty/resty#1274](https://github.com/go-resty/resty/pull/1274)** (Go) - Added CRLF (`\r\n`) and CR (`\r`) line-ending support to the SSE stream scanner (`splitSSEEvent` and `listenStream` in `sse.go`) per WHATWG HTML 9.2.5, fixing stalled event dispatch on non-LF servers and a race between `SSESource.Close` and `io.EOF`.
- **[UKGovernmentBEIS/inspect_ai#6078](https://github.com/UKGovernmentBEIS/inspect_ai/pull/6078)** (Python) - Extracted `urlparse(url).path` before file extension matching in `precomputed_scores()` so HTTP(S) presigned `.jsonl` URLs carrying query strings stop falling back to the `.json` reader.
- **[UKGovernmentBEIS/inspect_ai#5987](https://github.com/UKGovernmentBEIS/inspect_ai/pull/5987)** (Python) - Tagged blank model completions with `reason="no_response"` in `model_graded_qa` and `choice` scorers instead of grading empty strings.
- **[holoviz/panel#9090](https://github.com/holoviz/panel/pull/9090)** (Python) - Updated `FileDownload` in `panel/widgets/misc.py` to accept any `os.PathLike` object (such as `os.DirEntry` from `os.scandir`) rather than checking `isinstance(..., (str, Path))` only.
- **[holoviz/panel#9028](https://github.com/holoviz/panel/pull/9028)** (Python) - Fixed an inverted batch-update guard in `ReactiveESM._update_model` so `jslink` preprocessing hooks fire when child components are appended dynamically.
- **[holoviz/panel#8974](https://github.com/holoviz/panel/pull/8974)** (Python) - Scoped embedded widget state deduplication in `panel/io/embed.py` to require matching widget types and candidate option values before merging keys.
- **[holoviz/panel#8901](https://github.com/holoviz/panel/pull/8901)** (Python) - Guarded `DateRangeSlider._sync_values` in `panel/widgets/slider.py` against `value=None` before tuple unpacking.

Open pull requests under review:

- **[dexidp/dex#5100](https://github.com/dexidp/dex/pull/5100)** (Go) - Returns a typed `UserNotInRequiredGroupsError` (HTTP 403 Forbidden) instead of HTTP 500 when a GitHub OAuth user lacks required org or team membership in `connector/github/github.go`.
- **[super-productivity/super-productivity#11794](https://github.com/super-productivity/super-productivity/pull/11794)** (TypeScript) - Adds explicit connect and read timeouts to `CapacitorHttp` requests in `nativePostJson` so dropped mobile connections do not leave the SuperSync sign-in dialog spinning forever.

### Projects

- **[eSIM Price Truth](https://github.com/Jojoussef/esim-arbitrage-calculator)** ([live site](https://youssef-benatti.me/esim-arbitrage-calculator/)) - Zero-dependency Node static site generator that compiles a snapshot of 136,040 eSIM catalog prices across 94 destinations and 20 currencies into destination guides and an FX checkout calculator. Cross-references vendor pricing tables against European Central Bank spot rates to find checkout currencies that beat a buyer's home card rate, with Paddle webhook signature verification and Cloudflare Worker entitlement checks in front of the pro tools.
- **[Seha](https://github.com/Jojoussef/it-impact-app)** ([live demo](https://it-impact-app.vercel.app)) - Next.js 15 and TypeScript web application for digitizing and tracking Tunisian CNAM health insurance claims, built with NextAuth role gating and OCR intake pipelines.
- **[YuccaInfo GED](https://github.com/Jojoussef/yuccainfo_ged_backend)** ([backend](https://github.com/Jojoussef/yuccainfo_ged_backend) / [frontend](https://github.com/Jojoussef/yuccainfo_ged_frontend)) - Document archiving system built on Django REST Framework, PostgreSQL, and Next.js. Runs Tesseract OCR and transformer-based document classification on uploaded PDFs and scans.

### Contact

- Web: [youssef-benatti.me](https://youssef-benatti.me)
- Email: [contact@youssef-benatti.me](mailto:contact@youssef-benatti.me)
