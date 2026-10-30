# HopRefusalBench Theta evaluation results

Search and no-search outputs for **12 Theta model IDs**, with 889 questions per model and mode (21,336 response records).

[Download the results and checksum](https://github.com/sunxin000/HopRefusalBench-results/releases/tag/results-20261028)

## Model coverage

The current release covers **6 of the 10 model IDs evaluated in the [paper](https://arxiv.org/html/2608.01358v1#S4.SS1)** and 6 additional Theta model IDs.

**Qwen3.6-35B-A3B and DeepSeek-V4-Pro results are missing. The included DeepSeek-V4-Flash-0731 results belong to a different model and must not be reported as DeepSeek-V4-Pro.**

| Paper model | No-search records | Search records |
|---|---:|---:|
| GPT-5.4 | Not included | Not included |
| Claude-Sonnet-5 | Not included | Not included |
| Qwen3.5-397B-A17B | 889 | 889 |
| Kimi-K2.6 | 889 | 889 |
| Qwen3.6-35B-A3B | **Not included** | **Not included** |
| Qwen3.6-27B | 889 | 889 |
| Kimi-K2.5 | 889 | 889 |
| DeepSeek-V4-Pro | **Not included** | **Not included** |
| GLM-5.2 | 889 | 889 |
| GLM-5.1 | 889 | 889 |

Additional models included in both modes (889 records each):

- DeepSeek-V4-Flash-0731
- Ling-3.0-Flash
- Qwen3.5-122B-A10B
- Qwen3.8-27B
- aml_qwen36_heretic
- ling_flash_v3_safetyrl

The 12 included model IDs were exposed by the configured Theta credentials at collection time. On 2026-10-28, direct probes using the IDs Qwen3.6-35B-A3B and DeepSeek-V4-Pro returned HTTP 401 (SERVICE_NO_AUTH). Supplementary runs require authorized access or the corresponding deployment IDs. This does not establish that Theta lacks these models globally.

## Contents and scoring coverage

The archive contains original responses/search traces, evaluation reports, judge caches, run logs, summary.csv, package_manifest.json, the benchmark dataset, and archived paper references.

- No-search: all 10,668 cognitive-state judgments completed, with zero inference or state-judge errors.
- Search: all 10,668 responses and main cognitive-state outcomes are covered. The supplied search reports contain **56 failed auxiliary timeline judgments**, documented in package_manifest.json and summary.csv.
- API credentials and runtime environments are excluded.

## Integrity

Archive SHA-256:

```text
6e59b6a9127654191f0d27bc1fd63e794982f45a4870b36e7e3c5dd5f34f566a
```

Verify the download with the accompanying .sha256 file. After extraction, run `sha256sum -c SHA256SUMS` inside the extracted directory.

The published archive preserves the collected model IDs. This documentation update does not rename or relabel any result.
