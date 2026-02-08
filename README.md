# Edge-AI Defect Classification for Semiconductor Images

## Problem
Semiconductor manufacturing generates large volumes of inspection images. Manual and cloud-based inspection pipelines suffer from latency, bandwidth, and cost issues. This project proposes an Edge-AI based defect classification system using lightweight CNNs.

## Approach
- Use lightweight CNN (MobileNetV2 / EfficientNet-Lite)
- Train on wafer/industrial defect images
- Optimize and export model to ONNX
- Deployable on edge platforms (NXP eIQ compatible flow)

## Dataset Plan
- Public datasets: WM-811K, MVTec AD, NEU Surface Defect
- Minimum 500 images
- Classes: clean, other, defect_1, defect_2, ...
- Split into Train / Validation / Test

## Model
- Backbone: MobileNetV2 (Transfer Learning)
- Loss: Cross Entropy
- Optimizer: Adam
- Metrics: Accuracy, Precision, Recall, Confusion Matrix

## Code Structure
- train.py: training script
- evaluate.py: evaluation & metrics
- infer.py: single image inference
- export_onnx.py: export model to ONNX

## Edge Deployment
- Model will be quantized and exported to ONNX / TFLite
- Target: NXP eIQ runtime

## Status
Phase 1: Pipeline, structure, and methodology implemented.
Dataset ingestion and training to be finalized with organizer / public datasets.
