<div align="center">

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Weights_&_Biases-FFBE00?style=for-the-badge&logo=weightsandbiases&logoColor=black"/>
<img src="https://img.shields.io/badge/TensorBoard-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge"/>

<br/><br/>

# 🫀 BioDiffusion

### *Generative Modeling of Biomedical Signals using Diffusion Models*

<p align="center">
  <b>Synthesizing realistic physiological waveforms to address data scarcity in healthcare AI</b><br/>
  Denoising Diffusion Probabilistic Models (DDPM) · 1D U-Net Architecture · ECG Signal Generation
</p>

---

</div>

## 📌 Table of Contents

- [Overview](#-overview)
- [Motivation](#-motivation)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Project Structure](#-project-structure)
- [Results & Experiments](#-results--experiments)
- [Quickstart](#-quickstart)
- [Technologies](#-technologies)
- [Roadmap](#-roadmap)
- [Citation](#-citation)

---

## 🧬 Overview

**BioDiffusion** is a deep learning framework for **generating and analyzing biomedical time-series signals** using **Denoising Diffusion Probabilistic Models (DDPM)** paired with a **custom 1D U-Net architecture**.

The core idea: instead of collecting more patient data (which is expensive, privacy-sensitive, and often imbalanced), we *generate* realistic synthetic physiological signals that can augment training datasets for downstream healthcare AI tasks.

> 📓 The notebook `neural_network_research.ipynb` walks through the **complete pipeline** — from data preprocessing to training, evaluation, and signal visualization.

---

## 💡 Motivation

Biomedical datasets face three persistent challenges:

| Challenge | Impact |
|---|---|
| 🔒 **Privacy restrictions** | Limited sharing of patient data |
| ⚖️ **Class imbalance** | Rare conditions underrepresented |
| 📉 **Data scarcity** | Small datasets lead to overfitting |

Diffusion models offer a principled, high-fidelity approach to **synthetic data generation** — learning the true underlying distribution of physiological signals rather than producing simplistic interpolations.

---

## ✨ Key Features

- 🔁 **1D DDPM** — Full forward/reverse diffusion process adapted for time-series
- 🏗️ **Custom 1D U-Net** — Encoder–decoder with residual blocks and temporal conv layers
- 🎯 **Conditional & Unconditional Generation** — Class-free guidance support
- 📊 **End-to-end Pipeline** — Preprocessing → Training → Sampling → Evaluation
- 📈 **Experiment Tracking** — TensorBoard + Weights & Biases integration
- 🔬 **UMAP Visualization** — Latent space analysis of real vs. generated signals
- ⚡ **Progress Monitoring** — FastProgress / tqdm live feedback

---

## 🏛️ Architecture

```
Input Noise z_T  ──►  [Reverse Diffusion Process T → 0]  ──►  Synthetic ECG Signal
                              │
                    ┌─────────▼──────────┐
                    │    1D U-Net DDPM   │
                    │                    │
                    │  Encoder           │
                    │   │ Conv1D Blocks  │
                    │   │ Downsampling   │
                    │   ▼                │
                    │  Bottleneck        │
                    │   │ Timestep Emb.  │
                    │   ▼                │
                    │  Decoder           │
                    │   │ Upsampling     │
                    │   │ Residual Skip  │
                    │   ▼                │
                    │  Noise Prediction  │
                    └────────────────────┘
```

### Architectural Highlights

| Component | Description |
|---|---|
| **Encoder** | Temporal conv blocks with progressive downsampling |
| **Bottleneck** | Timestep-conditioned feature representation |
| **Decoder** | Symmetric upsampling with residual skip connections |
| **Timestep Embedding** | Sinusoidal positional encoding of diffusion step *t* |
| **Class Conditioning** | Optional class embeddings for guided generation |

---

## 📁 Project Structure

```
BioDiffusion/
│
├── 📓 neural_network_research.ipynb   # Main training & experimentation notebook
│
├── 📦 modules/
│   └── modules1D_cls_free.py          # Model architecture & diffusion utilities
│
├── 🗄️ datasets/                        # Raw & preprocessed dataset files
│
├── 💾 models/                          # Saved model checkpoints
│
└── 📤 outputs/                         # Generated signals & evaluation results
```

---

## 🔬 Results & Experiments

The notebook investigates the following research questions:

- ✅ Can DDPMs generate **morphologically faithful** ECG waveforms?
- ✅ How do **conditional vs. unconditional** models compare in signal fidelity?
- ✅ How does **diffusion timestep count** (*T*) affect generation quality?
- ✅ How stable is training over **extended runs**?

Generated signals are compared against real physiological recordings using:
- 📉 Visual waveform overlays
- 🗺️ UMAP latent space projections
- 📐 Morphological similarity metrics

---

## 🚀 Quickstart

### 1. Clone the Repository

```bash
git clone https://github.com/AmanKumar-23/BioDiffusion-Diffusion-Based-Generative-Model-for-Physiological-Stress-Signals.git
cd BioDiffusion
```

### 2. Install Dependencies

```bash
pip install torch torchvision numpy matplotlib scikit-learn tqdm wandb umap-learn fastprogress
```

> ⚠️ GPU recommended. Tested with Python 3.9+ and PyTorch 2.x.

### 3. Launch the Notebook

Open `neural_network_research.ipynb` using your preferred environment:

```bash
# Jupyter Notebook
jupyter notebook neural_network_research.ipynb

# VS Code
code .
# Then open the .ipynb file from the Explorer panel

# Google Colab
# Upload the notebook or open directly from GitHub
```

---

## 🛠️ Technologies

<div align="center">

| Category | Tools |
|---|---|
| **Deep Learning** | PyTorch |
| **Data Processing** | NumPy, Scikit-learn |
| **Visualization** | Matplotlib, UMAP |
| **Experiment Tracking** | TensorBoard, Weights & Biases |
| **Progress Monitoring** | tqdm, FastProgress |
| **Language** | Python 3.9+ |

</div>

---

## 🗺️ Roadmap

- [x] 1D DDPM implementation
- [x] U-Net backbone for time-series
- [x] Classifier-free guidance
- [x] W&B + TensorBoard logging
- [ ] FID-equivalent metric for biomedical signals
- [ ] Multi-lead ECG generation
- [ ] Conditional generation on patient metadata
- [ ] Web demo with Gradio / Streamlit

---

## 📎 Citation

If you use this work in your research, please cite:

```bibtex
@misc{biodiffusion2024,
  author       = {Aman Kumar},
  title        = {BioDiffusion: Generative Modeling of Biomedical Signals using Diffusion Models},
  year         = {2024},
  publisher    = {GitHub},
  url          = {https://github.com/AmanKumar-23/BioDiffusion-Diffusion-Based-Generative-Model-for-Physiological-Stress-Signals.}
}
```

---

<div align="center">

**Made with ❤️ and a lot of diffusion steps**

⭐ Star this repo if you find it useful — it helps others discover it!

</div>
