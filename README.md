# stroke-cct-classifier
A hybrid CNN-Transformer model for detecting and classifying brain strokes (Ischemia vs. Bleeding) from CT scans with Explainable AI (Grad-CAM &amp; Attention Maps)
-----------------------------------

A deep learning project utilizing a **Hybrid CNN-Transformer** architecture to classify brain CT scans. The model operates in two stages:
1. **Detection:** Differentiate between Normal vs. Abnormal scans.
2. **Classification:** Classify Abnormal scans into **Ischemic Stroke** or **Intracranial Bleeding**.

Includes Explainable AI (XAI) modules using **Grad-CAM** and **Self-Attention Rollout** to visualize model focus.

## Architecture
The model uses a `CompactConvTransformer`:
- **Stem:** 3-layer CNN to reduce high-def images (256x256) to feature maps (32x32).
- **Encoder:** 2-layer Transformer Encoder with custom hooks for attention extraction.
- **Head:** Linear classification head.
