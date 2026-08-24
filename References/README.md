# references/ — Studied Material for SIH26018

Reference repos cloned locally for offline study, paper mining, and architecture
comparison. **All are upstream projects — see their own licenses before reusing
code or assets.**

## Folder layout

```
references/
├── land-record-projects/   ← direct competitors / similar PS projects
├── paper-lists/            ← curated research-paper collections (cite from these)
├── ocr-engines/            ← OCR engines (cloned + notes on what wasn't)
└── README.md               ← this file
```

## land-record-projects/ (6 repos)
Directly comparable SIH / academic projects — study their architecture, then
differentiate.

| Folder | Upstream | Stars | What it does |
|---|---|---|---|
| `LandScan/` | officialankit18/-LandScan-OCR-Based-Land-Record-Digitization-Mapping-System | 0 | Tesseract OCR + Leaflet map; extracts owner, plot #, GPS from PDFs |
| `LEKH_AI/` | imrcoder07/LEKH_AI | 0 | Privacy-first OCR for land records, encrypted identity, tamper-proof storage |
| `land-record-mvp/` | kaustubh010/land-record-digitization-mvp | 1 | TypeScript MVP, modern stack |
| `Land-Record-Assistant/` | kaustubh010/Land-Record-Digitization-Assistant | 0 | Assistant variant of the above |
| `land-map-assistant/` | kaustubh010/land-map-assistant | 0 | GeoJSON-backed parcel map UI |
| `LandRecordDigitization-classic/` | anujkanetkar/LandRecordDigitization | 0 | Java-era (2018) baseline, SDL/DBMS course project |

## paper-lists/ (10 repos)
Curated markdown lists — mine these for citations in the literature-review
section of the final SIH report.

| Folder | Upstream | Stars | Topic |
|---|---|---|---|
| `awesome-document-understanding/` | tstanislawek/awesome-document-understanding | 1.5k | Document AI (OCR, KIE, VQA, tables) — **best single entry point** |
| `Awesome-DU-harrytea/` | harrytea/Awesome-Document-Understanding | 201 | Doc AI (smaller list) |
| `awesome-DU-datasets/` | ym-xu/awesome-document-understanding-datasets | 3 | Datasets (RVL-CDIP, FUNSD, CORD, SROIE…) |
| `awesome-ocr-resources/` | ZumingHuang/awesome-ocr-resources | 437 | OCR papers + datasets |
| `awesome-ocr-ChanChiChoi/` | ChanChiChoi/awesome-ocr | 400 | OCR papers |
| `AWESOME-OCR-LLM/` | Yuliang-Liu/AWESOME-OCR-LLM | 705 | OCR + LLMs (relevant to NLP layer) |
| `awesome-scene-text/` | chongyangtao/Awesome-Scene-Text-Recognition | 1.7k | Scene-text localization + recognition |
| `awesome-scene-text-detection/` | Charmve/awesome-scene-text-detection | 93 | Scene text detection |
| `awesome-scene-text-janzd/` | janzd/awesome-scene-text | 51 | Older scene text list |
| `awesome-nlp-papers/` | helboukkouri/awesome-nlp-papers | 35 | NLP papers by date — for validation/discrepancy layer |

## ocr-engines/ (2 cloned + notes)
Production OCR engines you can wire into SIH26018.

| Folder | Upstream | Stars | What it does |
|---|---|---|---|
| `RapidOCR/` | RapidAI/RapidOCR | 7.6k | Multi-backend OCR (ONNX / OpenVINO / MNN / Paddle / TensorRT / PyTorch) |
| `SimpleHTR/` | githubharald/SimpleHTR | 2.2k | Handwritten Text Recognition (CNN+BiLSTM+CTC) on IAM |
| `NOTES.md` | (this folder) | — | Engines NOT cloned (PaddleOCR 2GB, EasyOCR 162MB) with install commands |

## Quick links to upstream
- PaddleOCR (best Devanagari): https://github.com/PaddlePaddle/PaddleOCR
- EasyOCR: https://github.com/JaidedAI/EasyOCR
- LayoutLMv3 (HuggingFace): https://huggingface.co/microsoft/layoutlmv3-base
- TrOCR: https://huggingface.co/microsoft/trocr-base-handwritten
- Donut: https://huggingface.co/naver-clova-ix/donut-base

## How to use this folder
1. **Architecture study:** read `LandScan/` first — it's the closest end-to-end reference (Tesseract path).
2. **Privacy / security angle:** read `LEKH_AI/` — encrypted identity, tamper-proof storage patterns.
3. **Related work citations:** open `awesome-document-understanding/README.md`, scan for "Document VQA" and "Key Information Extraction", pick 5–8 papers relevant to land-record extraction.
4. **OCR engine choice:** see `ocr-engines/NOTES.md` for the install command matrix. Recommendation: **PaddleOCR** as primary, **EasyOCR** for prototyping speed.
