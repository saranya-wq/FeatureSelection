Below is a **professional `README.md` file for your GitHub repository** that includes references to both datasets you mentioned. It is written in a **research-grade format suitable for Zenodo archiving and journal reproducibility requirements**.

---

# README.md

# Hybrid Feature Selection Framework for IoMT Intrusion Detection

This repository contains the implementation of the research project:

**Hybrid Feature Selection for IoMT-Based Intrusion Detection System Integrating Mutual Information Filtering with Deep Learning-Based Accelerated Metaheuristic Optimization**

The project proposes a **two-stage hybrid feature selection framework** designed to enhance intrusion detection performance and computational efficiency in **Internet of Medical Things (IoMT)** environments.

The framework integrates **Mutual Information filtering** with a **Deep Learning–Enhanced Binary Dragonfly Algorithm (DL-BDA)** to identify optimal feature subsets for intrusion detection models.

---

# Overview

The rapid adoption of IoMT devices in healthcare has introduced new cybersecurity risks due to heterogeneous device communication protocols and limited device resources. These systems are vulnerable to attacks such as Denial-of-Service, reconnaissance attacks, spoofing, and protocol misuse.

To address these challenges, this project introduces a **hybrid feature selection framework** that combines:

1. **Mutual Information (MI) Filtering**

   A statistical filtering method that evaluates the dependency between network traffic features and class labels. Features are ranked based on MI scores and redundant features are removed using correlation analysis.

2. **Deep Learning–Enhanced Binary Dragonfly Algorithm (DL-BDA)**

   A wrapper-based metaheuristic optimization technique inspired by dragonfly swarm behavior. The algorithm incorporates:

   * Separation
   * Alignment
   * Cohesion
   * Attraction toward food sources
   * Avoidance of enemy positions

   A lightweight deep neural network (**ProxyNet**) is used as a surrogate fitness evaluator to reduce the computational cost of wrapper-based feature selection.

---

# Repository Structure

```
FeatureSelection/
│
├── data/
│   ├── dataset_loader.py
│
├── feature_selection/
│   ├── mutual_information_filter.py
│   ├── dragonfly_algorithm.py
│   ├── dl_bda_wrapper.py
│
├── baselines/
│   ├── genetic_algorithm_fs.py
│   ├── pso_feature_selection.py
│   ├── aco_feature_selection.py
│
├── models/
│   ├── proxynet.py
│   ├── classifiers.py
│
├── evaluation/
│   ├── metrics.py
│   ├── stability_analysis.py
│   ├── wilcoxon_test.py
│
├── experiments/
│   ├── run_pipeline.py
│
└── README.md
```

---

# Datasets

This project uses publicly available **IoMT network traffic datasets** for intrusion detection research.

## 1. CICIoMT2024 Dataset

Dataset Source:

The **CICIoMT2024 dataset** was developed by the Canadian Institute for Cybersecurity to provide a realistic benchmark for evaluating IoMT security solutions.

Key characteristics:

* Network traffic from **40 IoMT devices (25 real devices and 15 simulated devices)**
* Includes **18 different cyberattacks** targeting IoMT environments
* Multi-protocol traffic including **Wi-Fi, MQTT, and Bluetooth**
* Attack categories include:

  * DDoS
  * DoS
  * Reconnaissance
  * MQTT attacks
  * Spoofing attacks

The dataset captures device behavior across different lifecycle states, enabling the evaluation of advanced intrusion detection models.

---

## 2. IoMT Traffic Dataset

Dataset Source:
[https://www.kaggle.com/datasets/abhinavmangalore/iomt-traffic-data](https://www.kaggle.com/datasets/abhinavmangalore/iomt-traffic-data)

This dataset contains network traffic generated from IoMT device environments and includes multiple attack scenarios such as:

* HTTP-based DoS attacks
* ARP spoofing
* Network scanning
* MQTT flooding

The dataset provides network flow features extracted from packet captures, making it suitable for machine learning and deep learning–based intrusion detection systems.

---

# Installation

Clone the repository:

```bash
git clone https://github.com/saranya-wq/FeatureSelection.git
cd FeatureSelection
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Running Experiments

Run the complete feature selection pipeline:

```bash
python experiments/run_pipeline.py
```

This will execute:

1. Dataset preprocessing
2. Mutual Information feature filtering
3. DL-BDA wrapper optimization
4. Classifier training
5. Performance evaluation

---

# Evaluation Metrics

The framework evaluates intrusion detection performance using:

* Recall @ FPR ≤ 1%
* Precision–Recall AUC (PR-AUC)
* F1-score
* Balanced Accuracy
* ROC-AUC
* Feature Reduction Ratio
* Selection Runtime

Statistical validation includes:

* Wilcoxon Signed-Rank Test
* Feature subset stability using Jaccard similarity.

---

# Implementation Environment

The experiments were conducted using:

* Python 3.8
* PyTorch
* scikit-learn
* NumPy
* SciPy
* pandas

Hardware environment:

* Intel Xeon CPU
* NVIDIA Tesla GPU
* 64 GB RAM

---

# Reproducibility

All scripts required to reproduce the experimental results reported in the associated research study are included in this repository.

The repository contains:

* feature selection algorithms
* baseline comparison methods
* model training scripts
* statistical analysis modules

---

# Code Archive (DOI)

The complete implementation has been archived in Zenodo to ensure reproducibility.

DOI:

[https://doi.org/10.5281/zenodo.18987427](https://doi.org/10.5281/zenodo.18987427)

---

# Citation

If you use this code in your research, please cite the corresponding publication associated with this repository.

---

# License

This repository is provided for **research and academic purposes**.

---

If you want, I can also generate **three files that journals and Zenodo strongly prefer**:

1. **`CITATION.cff` file** (auto-citation support for GitHub + Zenodo)
2. **`requirements.txt` file for your project**
3. **`reproducibility.md` file (very helpful for reviewers)**.
