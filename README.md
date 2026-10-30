# HopRefusalBench combined results — 2026-10-30

<!-- combined-results-20261030 -->

[Download the combined results](https://github.com/sunxin000/HopRefusalBench-results/releases/download/results-20261030/hoprefusalbench_all_results_20261030.tar.gz) · [Release and checksum](https://github.com/sunxin000/HopRefusalBench-results/releases/tag/results-20261030) · [Coverage table](results_20261030/coverage.csv) · [Machine-readable manifest](results_20261030/package_manifest.json)

This is the latest combined artifact. Earlier releases remain available; their original files are unchanged.

This package combines the original 12-model search/no-search results, completed no-search supplements for Qwen3.6-35B-A3B and DeepSeek-V4-Pro, Qwen3.5-397B-A17B thinking-enabled no-search, and the latest supplied three search runs.

**14 distinct models, 30 experimental conditions, 26,665 response records.** Conditions separate thinking settings and search modes.

## Coverage to retain when reporting results

- 29 conditions have all 889 main outcomes. The supplied Qwen3.5-397B-A17B thinking-enabled search run has **884/889 responses** and **3 state-judge errors**; its reported rates use **881 valid outcomes**. The five missing IDs are listed in package_manifest.json.
- There are **60 auxiliary timeline-judge errors** across the supplied search runs, itemized per condition. A supplied report may set all_complete=true even when judging failed; use the explicit error counters and computed coverage here.
- Qwen397B thinking-enabled no-search has 98 token-capped responses and 95 empty final answers. These observed outputs are retained and scored; they are not missing inference records.
- The DeepSeek paper-model supplement is **DeepSeek-V4-Pro**. **DeepSeek-V4-Flash-0731** is retained as a separate additional model.
- Search-only files in the latest user archive do not include their runtime manifest; thinking labels follow the supplied source directory names.
- Results for GPT-5.4 and Claude-Sonnet-5 remain absent. No missing answer or failed judgment was filled during packaging.

## Layout

- results/{thinking_disabled,thinking_enabled}/{no_search,search}/{model}/: canonical responses/traces, reports, judge caches, and logs.
- audit/: original retry/checkpoint files, excluded from the canonical sample totals.
- provenance/: supplied run configurations, preflights, source/runtime references, and archived documentation.
- summary.csv / coverage.csv / package_manifest.json: per-condition metrics, denominators, coverage, and source mapping.
- dataset/: the exact 889-question benchmark.

All canonical files are byte-preserving copies. No .env credentials or runtime environments are included. Verify extracted files from this directory with `sha256sum -c SHA256SUMS`.

## Main metrics

| Model | Mode | Thinking | Responses | Metric N | State errors | Timeline errors | TCHR | SHDR |
|---|---|---|---:|---:|---:|---:|---:|---:|
| DeepSeek-V4-Flash-0731 | no_search | off | 889/889 | 889 | 0 | 0 | 28.46 | 66.25 |
| GLM-5.1 | no_search | off | 889/889 | 889 | 0 | 0 | 25.87 | 72.55 |
| GLM-5.2 | no_search | off | 889/889 | 889 | 0 | 0 | 26.77 | 71.32 |
| Kimi-K2.5 | no_search | off | 889/889 | 889 | 0 | 0 | 34.53 | 61.53 |
| Kimi-K2.6 | no_search | off | 889/889 | 889 | 0 | 0 | 37.35 | 56.92 |
| Ling-3.0-Flash | no_search | off | 889/889 | 889 | 0 | 0 | 19.12 | 77.17 |
| Qwen3.5-122B-A10B | no_search | off | 889/889 | 889 | 0 | 0 | 38.02 | 54.67 |
| Qwen3.5-397B-A17B | no_search | off | 889/889 | 889 | 0 | 0 | 40.72 | 54.33 |
| Qwen3.6-27B | no_search | off | 889/889 | 889 | 0 | 0 | 34.08 | 46.79 |
| Qwen3.8-27B | no_search | off | 889/889 | 889 | 0 | 0 | 31.95 | 56.81 |
| aml_qwen36_heretic | no_search | off | 889/889 | 889 | 0 | 0 | 17.77 | 76.83 |
| ling_flash_v3_safetyrl | no_search | off | 889/889 | 889 | 0 | 0 | 38.25 | 52.08 |
| DeepSeek-V4-Flash-0731 | search | off | 889/889 | 889 | 0 | 6 | 15.52 | 29.92 |
| GLM-5.1 | search | off | 889/889 | 889 | 0 | 7 | 14.62 | 34.20 |
| GLM-5.2 | search | off | 889/889 | 889 | 0 | 3 | 13.84 | 27.22 |
| Kimi-K2.5 | search | off | 889/889 | 889 | 0 | 11 | 18.22 | 39.48 |
| Kimi-K2.6 | search | off | 889/889 | 889 | 0 | 1 | 23.51 | 37.68 |
| Ling-3.0-Flash | search | off | 889/889 | 889 | 0 | 6 | 7.65 | 32.17 |
| Qwen3.5-122B-A10B | search | off | 889/889 | 889 | 0 | 1 | 32.85 | 39.93 |
| Qwen3.5-397B-A17B | search | off | 889/889 | 889 | 0 | 0 | 41.51 | 51.07 |
| Qwen3.6-27B | search | off | 889/889 | 889 | 0 | 1 | 16.20 | 27.90 |
| Qwen3.8-27B | search | off | 889/889 | 889 | 0 | 1 | 28.35 | 32.96 |
| aml_qwen36_heretic | search | off | 889/889 | 889 | 0 | 1 | 20.25 | 74.24 |
| ling_flash_v3_safetyrl | search | off | 889/889 | 889 | 0 | 18 | 15.30 | 37.12 |
| DeepSeek-V4-Pro | no_search | off | 889/889 | 889 | 0 | 0 | 30.82 | 64.79 |
| Qwen3.6-35B-A3B | no_search | off | 889/889 | 889 | 0 | 0 | 32.73 | 60.40 |
| Qwen3.5-397B-A17B | no_search | on | 889/889 | 889 | 0 | 0 | 35.66 | 51.86 |
| DeepSeek-V4-Pro | search | off | 889/889 | 889 | 0 | 0 | 17.44 | 34.20 |
| Qwen3.6-35B-A3B | search | off | 889/889 | 889 | 0 | 1 | 30.03 | 57.82 |
| Qwen3.5-397B-A17B | search | on | 884/889 | 881 | 3 | 3 | 40.18 | 53.58 |

[Previous coverage documentation](docs/archive/README-before-results-20261030.md)
