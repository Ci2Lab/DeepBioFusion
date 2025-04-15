# # 🌲 DeepBioFusion: Tree-Level Above Ground Biomass (AGB) Estimation using Multi-Modal Deep Learning

This repository contains the complete code and supporting material for our study on individual tree-level estimation of Above Ground Biomass (AGB) using multi-modal remote sensing data and deep learning. The proposed model does **not rely on LiDAR data for prediction**, making it suitable for operational scalability across large forested regions.

---

## 🔍 Overview

Accurate AGB estimation plays a crucial role in forest carbon accounting and ecological monitoring. Traditional approaches rely heavily on field data or LiDAR, which are costly and difficult to scale. This study introduces **DeepBioFusion**, a CNN-based architecture that fuses:

- 🛰️ Optical imagery (e.g., RGB or multispectral)
- 📡 Synthetic Aperture Radar (SAR) data (X, C, and L bands)
- 🌳 Tree species maps derived from the Norwegian Forest Inventory

---

## 🧠 Key Contributions

- 🚫 **LiDAR-free prediction**: Model predicts biomass without needing LiDAR input at inference.
- 🌐 **Scalable design**: Adaptable to any region with satellite access.
- 🌲 **Individual tree resolution**: Focused on single-tree level predictions.
- 📉 **High accuracy**: Achieved **MAE ≈ 1.2 kg** and **RMSE ≈ 1.5 kg** per tree.
- 🔁 **Reproducible workflow**: Includes complete pipeline for training and evaluation.

---

## 🧪 Methodology

The end-to-end pipeline includes segmentation, patch extraction, species labeling, and biomass estimation using a multi-branch CNN.

### 📌 Methodology Diagram

<p align="center">
  <img src="images/methodology_diagram.png" width="700"/>
</p>




---

## 🧬 Visual Samples from the Paper

### 🗺️ AGB Distribution Map

<p align="center">
  <img src="images/agb_map.png" width="600"/>
</p>

### 🌳 Tree Species Classification Map

<p align="center">
  <img src="images/species_distribution.png" width="600"/>
</p>

### 📉 Model Performance Chart

<p align="center">
  <img src="images/mae_rmse_chart.png" width="600"/>
</p>




Our model shows strong performance across various tree species categories, and outperforms several existing approaches that rely heavily on field-collected or LiDAR data.

---

## 🧰 Setup

### 📦 Installation

```bash
git clone https://github.com/yourusername/DeepBioFusion.git
cd DeepBioFusion
pip install -r requirements.txt
