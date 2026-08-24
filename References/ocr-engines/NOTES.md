# OCR Engine References — NOT Cloned Locally

These repos are too large to clone into the references bundle (>100MB each,
mostly model weights + training data). Cloned locally below if they're small
enough. For the giants, refer to upstream.

## Cloned locally
- **RapidOCR** — multi-backend OCR (ONNX, OpenVINO, MNN, Paddle, TensorRT, PyTorch)
- **SimpleHTR** — handwritten text recognition with TensorFlow (CNN+BiLSTM+CTC)

## Use upstream instead (DO NOT CLONE — too big)
- **PaddlePaddle/PaddleOCR** (~2 GB)
  https://github.com/PaddlePaddle/PaddleOCR
  ⭐ 88k. Best Devanagari OCR quality. Use for the primary engine.
- **JaidedAI/EasyOCR** (~162 MB, ~80 langs incl. Devanagari)
  https://github.com/JaidedAI/EasyOCR
  ⭐ 30k. Fast to install, Python API, good for a quick prototype.

## Other engines worth noting (not in scope of this PS)
- tesseract-ocr/tesseract — classic Tesseract (used by LandScan reference).
- PaddlePaddle/PaddleSeg — segmentation models for layout extraction.
- huggingface/transformers — for LayoutLMv3, TrOCR, Donut.

## Install cheat sheet (for the actual SIH26018 build)

```bash
# Primary OCR engine (Devanagari + 100 langs)
pip install paddleocr paddlepaddle

# Lightweight alternative
pip install easyocr

# Cross-platform / mobile
pip install rapidocr-onnxruntime

# Document AI / field extraction (transformers)
pip install transformers torch torchvision
# LayoutLMv3, TrOCR, Donut are all available via Hugging Face

# Classic Tesseract (fallback)
# Windows: choco install tesseract
# Linux: sudo apt install tesseract-ocr tesseract-ocr-hin tesseract-ocr-mar
```
