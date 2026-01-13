# Multi-Modal Generative Video System for Skincare Product Outcome Visualization

## Overview
Skincare brands invest heavily in marketing to demonstrate product effectiveness, yet producing personalized, high-quality visual content at scale remains expensive and time-consuming. This project addresses that gap by building a **multi-modal generative AI system** that creates **personalized before-and-after skincare product outcome videos**.

Given a skincare product’s ingredient information and a face image representing a specific skin condition, the system generates a **temporally consistent video** that visually simulates product usage and potential skin improvements over time. The output is designed for **marketing visualization and consumer education**, not medical diagnosis.

---

## What This System Does
- Accepts **product ingredient text**, **face images**, and **skin context**
- Encodes product effects and facial skin characteristics
- Generates realistic **before-and-after outcome videos**
- Ensures temporal consistency across frames
- Produces **marketing-ready video outputs**

---

## What This System Does NOT Do
- ❌ Provide medical or dermatological advice  
- ❌ Predict guaranteed clinical outcomes  
- ❌ Diagnose skin conditions  

This system is intended solely for **visual simulation and marketing demonstration purposes**.

---

## High-Level Pipeline

1. **Product Understanding**
   - Encodes ingredient text into semantic product-effect embeddings

2. **Face & Skin Encoding**
   - Extracts identity-preserving facial and skin features from images

3. **Conditional Outcome Modeling**
   - Combines product, face, skin type, and temporal context

4. **Generative Video Modeling**
   - Uses conditional diffusion to generate sequential video frames

5. **Temporal Consistency Refinement**
   - Reduces flicker and preserves identity across frames

6. **Video Assembly & Output**
   - Produces final MP4/WebM videos suitable for marketing use

---

## Input / Output Contract

### Input
```yaml
product_text: string
face_image: image
skin_type: [normal, acne_prone, sensitive, oily, dry]
usage_duration_days: int

