🌱 Exploring Greenhouse Pest Detection Using
Grounding DINO, SAM, and CLIP Embeddings
---
📌 Overview

This project explores a small-object detection and segmentation system for greenhouse pest monitoring, with a focus on whiteflies and aphids.
It combines Grounding DINO, Segment Anything Model (SAM), and CLIP embeddings, enhanced by SAHI, to detect pests using text prompts with minimal training.

Developed as part of a University Computer Vision course, this project investigates the effectiveness of modern foundation models in agricultural vision tasks.
---
🎯 Motivation

Greenhouse pest detection is challenging due to:

Extremely small object sizes

Dense clustering of insects

Complex and cluttered backgrounds

Traditional object detectors often struggle in such conditions. This project evaluates whether zero-shot detection and segmentation models, guided by language prompts, can provide a flexible and robust alternative.
---
🧠 System Architecture

The system consists of the following components:

🔹 Grounding DINO

Zero-shot object detector guided by text prompts

Produces bounding boxes for target pests (e.g., “whitefly”, “aphid”)

🔹 SAHI (Slicing Aided Hyper Inference)

Improves detection of small and densely packed objects

Splits images into overlapping tiles before inference

🔹 Segment Anything Model (SAM)

Generates high-quality segmentation masks

Uses bounding boxes from Grounding DINO as prompts

🔹 CLIP Embeddings

Provides semantic verification

Ensures detected regions align with the intended text prompts
---
📂 Dataset

Source: Custom dataset created and managed using Roboflow

Content: Greenhouse images containing whiteflies and aphids

Usage:

Used for analysis and statistics

Detection relies on zero-shot inference, not supervised training
---
⚙️ Methodology

Images are sliced using SAHI to enhance small-object detection.

Grounding DINO detects pests based on text prompts.

Detected bounding boxes are passed to SAM to generate segmentation masks.

CLIP embeddings verify semantic consistency between detections and target classes.

Final results are visualized with bounding boxes and segmentation masks.
---
📊 Results

Successful detection and segmentation of whiteflies and aphids

Improved performance on small objects using SAHI

Accurate and interpretable visual outputs suitable for monitoring tasks
---
▶️ How to Run (Google Colab)

Open the notebook in Google Colab.

Run the initial setup cell first (before downloading Grounding DINO).

Update the supervision library as instructed in the notebook.

Restart the runtime after updating dependencies.

Run all cells from top to bottom.

Provide input images and text prompts to perform detection.
---
🖼️ Outputs

Bounding boxes around detected pests

Segmentation masks highlighting pest regions

Visualized results displayed directly in the notebook
