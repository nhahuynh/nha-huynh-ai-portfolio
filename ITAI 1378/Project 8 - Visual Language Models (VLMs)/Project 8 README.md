# Vision–Language Modeling: CLIP & BLIP

This README documents a project exploring Visual Language Models and their capabilities for classification and caption generation.

---

## Problem Statement

Images and text are represented differently (pixels vs. encoded characters), creating a **representation gap** that makes aligning vision and language challenging.

## Approach

I compared:

- **CLIP** for zero-shot classification (matching existing images to existing text)
- **BLIP** for caption generation (producing new text)

I evaluated BLIP’s captions, tested prompt influence, and analyzed what is needed to fine-tune VLMs for specialized tasks like X-ray interpretation.

## Results

- BLIP correctly captioned **5 of 6** images.
- One image was misinterpreted (boy + ox).
- BLIP hallucinated by counting humans as animals.
- More precise prompts produced more accurate descriptions.

## Key Findings

- Pretrained BLIP would **not** work for medical imaging without fine-tuning.
- Freeze most layers and train only the last few to avoid overfitting and save compute.
- Aggressive fine-tuning on small datasets leads to overfitting.
- Data quality strongly affects reliability; low-quality data increases hallucinations.

## Technologies Used

- Python
- HuggingFace Transformers
- PyTorch

## How to Run

1. Open notebook file L08_Huynh_Nha_ITAI1378.ipynb in Google Colab.
2. Run cells sequentially
