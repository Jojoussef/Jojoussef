# Youssef Benatti

AI and data engineer in Monastir, Tunisia. I build schema-migration engines, real-time ingestion pipelines, and document extraction systems in Python, SQL, Go, and TypeScript, and patch upstream open-source libraries when I run into bugs along the way.

### Data Engineering & Applied AI Projects

- **Intelligent Financial Data Migration Engine (`PFE` / `smart-migration-service`)** - Automated ETL and schema-mapping platform for migrating legacy banking and leasing databases (`Cassiopae`, `EVOLAN`, Oracle, PostgreSQL) into `Xloan`. Introspects source and target DDL (`migration/schema/`), generates candidate field mappings using weighted semantic scoring and a Neo4j / Apache AGE GraphRAG knowledge base (`migration/mapping/`), and compiles validated JSON mappings into declarative **dbt** SQL models (`dbt_compiler.py`) and Talend jobs. Executes AI-generated SQL inside an ephemeral PostgreSQL sandbox (`migration/agent/sandbox.py`, `auto_healer.py`) with statement timeouts, automatic syntax remediation, OpenLineage UUIDv5 lineage tracking, and 26 `pytest` suites.
- **[eSIM Price Truth & FX Pipeline](https://github.com/Jojoussef/esim-arbitrage-calculator)** ([live site](https://youssef-benatti.me/esim-arbitrage-calculator/)) - Zero-dependency Node data pipeline and static generator that normalizes 136,040 scraped eSIM price points (6,802 plan variants across 94 destinations and 20 currencies) against European Central Bank spot rates to detect 224 currency inversions. Exposes flat dataset exports and live price-anomaly feeds behind HMAC-signed Cloudflare Worker and Appwrite Function gates.
- **Adelaide Emergency Department Real-Time ETL (`sa-ed-dashboard`)** ([live dashboard](https://sa-ed-dashboard.vercel.app)) - Time-series ingestion and monitoring pipeline polling 9 South Australia Health Emergency Department feeds (`ED001`-`ED009`) every 15 minutes via authenticated cron workers (`app/api/cron/ed-data`). Persists occupancy, triage wait-time, and ambulance stream snapshots in PostgreSQL with automated gap detection (`app/api/monitor/data-continuity`) and 48-point rolling window aggregation.
- **BVMT Financial Market RAG & Forecasting (`stockx-pt-backend`)** ([live app](https://stockx-pt-frontend.vercel.app)) - Hybrid SQL and vector retrieval backend for Tunisian stock exchange (BVMT / BIAT) market data. Syncs PostgreSQL financial news into ChromaDB using `all-MiniLM-L6-v2` embeddings (`load_pg_to_chroma.py`), classifies user query intent (`chatbot.py`) to route between deterministic SQL KPI aggregations (`kpi_queries.py`) and Hugging Face RAG synthesis, and serves time-series price forecasts.
- **[YuccaInfo GED](https://github.com/Jojoussef/yuccainfo_ged_backend)** ([backend](https://github.com/Jojoussef/yuccainfo_ged_backend) / [frontend](https://github.com/Jojoussef/yuccainfo_ged_frontend)) & **[Seha](https://github.com/Jojoussef/it-impact-app)** ([live demo](https://it-impact-app.vercel.app)) - Document OCR and zero-shot classification pipelines. YuccaInfo extracts text from uploaded PDFs and scans via `pytesseract` on Django REST + PostgreSQL and classifies documents into 9 categories with `facebook/bart-large-mnli`. Seha digitizes and tracks Tunisian CNAM health insurance claims in Next.js 15.
- **Multi-Provider Biometric & Document OCR (`id-verification`)** ([live demo](https://id-verification-pearl.vercel.app)) - Identity verification pipeline in Next.js 15 and Sharp (`app/api/ocr`, `app/api/face-match`, `app/api/liveness`) integrating Scandit ID capture and CompreFace with automatic fallback across AWS Textract/Rekognition, Google Cloud Vision, and Azure Face API.

### Upstream Open-Source Patches

Merged pull requests in AI evaluation, data visualization, and networking libraries:

- **[UKGovernmentBEIS/inspect_ai#6078](https://github.com/UKGovernmentBEIS/inspect_ai/pull/6078)** (Python) - Extracted `urlparse(url).path` before file extension matching in `precomputed_scores()` so HTTP(S) presigned `.jsonl` URLs carrying query strings stop falling back to the `.json` reader.
- **[UKGovernmentBEIS/inspect_ai#5987](https://github.com/UKGovernmentBEIS/inspect_ai/pull/5987)** (Python) - Tagged blank model completions with `reason="no_response"` in `model_graded_qa` and `choice` scorers instead of grading empty strings.
- **[holoviz/panel#9090](https://github.com/holoviz/panel/pull/9090)** (Python) - Updated `FileDownload` in `panel/widgets/misc.py` to accept any `os.PathLike` object (such as `os.DirEntry` from `os.scandir`) rather than checking `isinstance(..., (str, Path))` only.
- **[holoviz/panel#9028](https://github.com/holoviz/panel/pull/9028)** (Python) - Fixed an inverted batch-update guard in `ReactiveESM._update_model` so `jslink` preprocessing hooks fire when child components are appended dynamically.
- **[holoviz/panel#8974](https://github.com/holoviz/panel/pull/8974)** (Python) - Scoped embedded widget state deduplication in `panel/io/embed.py` to require matching widget types and candidate option values before merging keys.
- **[holoviz/panel#8901](https://github.com/holoviz/panel/pull/8901)** (Python) - Guarded `DateRangeSlider._sync_values` in `panel/widgets/slider.py` against `value=None` before tuple unpacking.
- **[go-resty/resty#1274](https://github.com/go-resty/resty/pull/1274)** (Go) - Added CRLF (`\r\n`) and CR (`\r`) line-ending support to the SSE stream scanner (`splitSSEEvent` and `listenStream` in `sse.go`) per WHATWG HTML 9.2.5, fixing stalled event dispatch on non-LF servers and a race between `SSESource.Close` and `io.EOF`.

Open pull requests under review:

- **[dexidp/dex#5100](https://github.com/dexidp/dex/pull/5100)** (Go) - Returns a typed `UserNotInRequiredGroupsError` (HTTP 403 Forbidden) instead of HTTP 500 when a GitHub OAuth user lacks required org or team membership in `connector/github/github.go`.
- **[super-productivity/super-productivity#11794](https://github.com/super-productivity/super-productivity/pull/11794)** (TypeScript) - Adds explicit connect and read timeouts to `CapacitorHttp` requests in `nativePostJson` so dropped mobile connections do not leave the SuperSync sign-in dialog spinning forever.

### Contact

- Web: [youssef-benatti.me](https://youssef-benatti.me)
- Email: [contact@youssef-benatti.me](mailto:contact@youssef-benatti.me)
