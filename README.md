Exploring Greenhouse Pest Detection Using Grounding DINO, SAM, and CLIP Embeddings
Overview

This project explores a small-object detection and segmentation system for greenhouse pest monitoring, focusing on two common pests: whiteflies and aphids.
The system combines Grounding DINO, SAM (Segment Anything Model), and CLIP embeddings, enhanced with SAHI, to detect and segment small, densely packed pests using text prompts with minimal training.

The project was developed as part of a Computer Vision course at university and serves as an experimental exploration of modern foundation models for agricultural applications.

Motivation

Detecting greenhouse pests is challenging due to:

Small object sizes

Dense clustering

Complex backgrounds

Traditional detectors often struggle in these conditions. This project investigates whether zero-shot and foundation models, guided by language prompts and segmentation, can provide a flexible and effective alternative with minimal dataset-specific training.

System Architecture

The pipeline consists of the following components:

Grounding DINO

A zero-shot object detector guided by text prompts

Produces bounding boxes for specified pest classes (e.g., “whitefly”, “aphid”)

SAHI (Slicing Aided Hyper Inference)

Improves detection of small and densely packed objects

Splits images into overlapping tiles before detection

SAM (Segment Anything Model)

Generates segmentation masks from detected bounding boxes

CLIP Embeddings

Used for semantic verification of detected segments

Helps ensure detected objects align with the intended textual concept

Dataset

Source: Custom dataset created and managed using Roboflow

Content: Greenhouse images containing whiteflies and aphids

Usage:

Used primarily for evaluation and statistics

The detection itself relies on zero-shot inference, not supervised training

Methodology

Input images are processed using SAHI to enhance small-object detection.

Grounding DINO detects pests based on text prompts.

Detected bounding boxes are passed to SAM to generate segmentation masks.

CLIP embeddings are used to verify semantic consistency between detected regions and the target pest classes.

Final outputs include bounding boxes and segmentation masks overlaid on the original images.

Results

The system successfully detected and segmented whiteflies and aphids in greenhouse images.

SAHI significantly improved detection performance for small and clustered pests.

The combined architecture produced visually accurate bounding boxes and segmentation masks, demonstrating the effectiveness of foundation models for agricultural vision tasks.

How to Run (Google Colab)

Open the notebook in Google Colab.

Important:

Run the initial setup cell first (before downloading Grounding DINO).

Update the supervision library as instructed in the notebook.

Restart the runtime after updating dependencies.

Run all cells again from top to bottom.

Provide images and text prompts to perform detection and segmentation.

Outputs

Bounding boxes around detected pests

Segmentation masks highlighting pest regions

Visualized results directly within the Colab notebook
