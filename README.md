# 🎯 TMT - Efficiently Align Multiple Objectives

[![Download TMT](https://img.shields.io/badge/Download_TMT-v1.0-blue)](https://github.com/Jiroo00/TMT/releases)

## 🚀 Getting Started

Welcome to TMT, a tool designed to help you tackle complex optimization problems using Tchebycheff scalarization. This guide will walk you through downloading and running TMT efficiently, even if you have no technical background.

## 📥 Download & Install

To get started, visit the [Releases page](https://github.com/Jiroo00/TMT/releases) to download the latest version of TMT. Download the appropriate file for your system and follow the installation instructions below.

### 🛠️ Installation Steps

1. **Install Anaconda:** 
   If you don’t have Anaconda installed, download it from the [Anaconda website](https://www.anaconda.com/products/distribution#download-section) and follow the installation instructions specific to your operating system.

2. **Create a New Environment:**
   Open your terminal (or Anaconda Prompt for Windows) and run the following commands:

   ```bash
   conda create -n tmt python=3.10
   conda activate tmt
   ```

3. **Clone Required Repositories:**
   You will need to clone some repositories for TMT to function properly. Run these commands one by one:

   ```bash
   git clone https://github.com/eth-sri/language-model-arithmetic.git
   cd language-model-arithmetic/
   pip install -e .
   cd ..
   
   git clone https://github.com/huggingface/peft.git
   cd peft/
   pip install -e .
   cd ..
   
   conda install -c nvidia cuda-compiler
   ```

4. **Clone the Main TMT Repository:**

   ```bash
   git clone https://github.com/PKU-Alignment/safe-rlhf.git
   cd safe-rlhf
   pip install .
   cd ..
   ```

5. **Install Additional Requirements:**

   ```bash
   pip install -r requirements.txt
   ```

### ⚙️ Preparing Data

Before using TMT, you need to prepare your data. Here’s how to do it:

1. Navigate to the data folder:

   ```bash
   cd code/data  # or code/data/hh
   ```

2. Run the following scripts to organize your data:

   ```bash
   python relabel.py
   python relabel_hh.py
   ```

### 🎓 Training the Model

To train your model, follow these steps:

1. Navigate to the training directory:

   ```bash
   cd code/training
   ```

2. Start the training process by executing:

   ```bash
   bash run.sh
   ```

### 📊 Evaluating the Model

After training, you can evaluate your model as follows:

1. Go to the evaluation directory:

   ```bash
   cd code/evaluation  # or code/hh/evaluation
   ```

2. Run the evaluation scripts:

   ```bash
   bash generation.sh
   bash compute_reward.sh
   ```

These evaluations will help you understand how well your model aligns with some predefined multi-objective criteria.

## 🌟 Features

- **Tchebycheff Scalarization:** Effectively captures non-convex Pareto frontiers in optimization challenges.
- **User-Friendly Interface:** Designed for users without programming expertise.
- **Comprehensive Data Handling:** Easily prepare data and evaluate models.

## 📄 Documentation

For more details on using TMT and its various capabilities, consult the documentation within the repository. 

## 💬 Support

If you encounter any issues or have questions, please feel free to raise them in the repository's issues section. Your feedback helps improve TMT for everyone.

Remember to visit the [Releases page](https://github.com/Jiroo00/TMT/releases) to download the latest version of TMT and stay updated on new features and improvements.