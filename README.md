# 🧠 EEG-Based Stress Prediction Using Neural Networks

## 🧾 Overview

This repository contains the code and resources for a deep learning project focused on predicting stress states using EEG signals.  

EEG-based stress recognition has immense potential in real-time brain-computer interfaces (BCI), cognitive research, and mental health support. This project leverages deep learning, particularly LSTM networks, to classify EEG signals into *calm* and *stress* states.

This project was completed as part of the **Big Data Analytics** module at the **National Institute of Posts & Telecommunications (INPT), Rabat**.

---

## 🎯 Objective

The goal is to build an accurate and robust model that can distinguish between stress-induced and calm EEG states using temporal neural networks.  

By analyzing EEG signal patterns during both cognitive tasks and relaxation, the model aims to assist in real-time stress monitoring applications.

---

## 📂 Dataset

The project uses the publicly available **SAM40 EEG Dataset**, which contains EEG recordings from 40 subjects exposed to cognitive stress through:

- 🧪 Stroop Color-Word Test  
- ➕ Arithmetic Problem Solving  
- 🔁 Mirror Image Recognition  
- 🧘 Relaxation Test  

The dataset was reorganized into:

- `stress/` – EEG segments recorded during stress-inducing tasks  
- `calm/` – EEG segments recorded during relaxation  

🔗 **Dataset Link:**  
[https://figshare.com/articles/dataset/SAM_40_Dataset...](https://figshare.com/articles/dataset/SAM_40_Dataset_of_40_Subject_EEG_Recordings_to_Monitor_the_Induced-Stress_while_performing_Stroop_Color-Word_Test_Arithmetic_Task_and_Mirror_Image_Recognition_Task/14562090/1?file=27956376)  
📄 **Related Paper:** [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2352340921010465)  
🧘 **Calm State Dataset:** [Mendeley Data](https://data.mendeley.com/datasets/8c26dn6c7w/1)

---

## 🧼 Preprocessing

EEG signals were preprocessed through a custom pipeline involving:

- Band-pass filtering (0.5–45 Hz)  
- Artifact removal via:
  - Savitzky-Golay smoothing  
  - Wavelet thresholding  

---

## 🧠 Model Development

The model architecture is based on a **Long Short-Term Memory (LSTM)** neural network, ideal for sequential EEG data.  

✅ **Model Accuracy:** Achieved **96%** classification accuracy between calm and stress states.

---

## 🧪 Test Performance

The trained model was evaluated on two specific EEG samples:

- `Corrupted_EEG.mat` → from **SAM40 (stress category)**  
- `S001E01.edf` → from **Fusion dataset (calm category)**  

These tests confirmed the model's generalizability across different EEG sources.

---

## 🛠️ Features

- EEG signal preprocessing with advanced filtering and artifact reduction  
- LSTM-based deep learning classifier for temporal EEG data  
- Real-time stress state prediction on unseen data  
- Full model training pipeline in Jupyter Notebook  
- Model and results ready for deployment or extension

---

## 📁 Project Structure

```
├── EEG-Stress_Prediction_Project_Final.ipynb   # Jupyter Notebook with full workflow
├── EEG_Stress_Prediction_Presentation.pdf      # English Project Presentation
└── README.md                                   # Project documentation
```

---

## ⚙️ Installation

Follow the steps below to set up and run the project locally.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/EEG-Stress-Prediction.git
cd EEG-Stress-Prediction
```

### 2. Set Up Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate     # On Windows: venv\Scripts\activate
```
---

## 🚀 How to Use

### ▶️ Run the Jupyter Notebook

To explore the full project workflow:

```bash
jupyter notebook EEG-Stress_Prediction_Project_Final.ipynb
```

This notebook includes:

- Data loading and preprocessing  
- Model training and evaluation  
- Test predictions on external EEG data
