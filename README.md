# 🛡️ Enhanced Deep Learning Techniques to Detect Trojan Horse Attack in Cybersecurity

> **Major Project Report — B.Tech Computer Science & Engineering**  
> Vel Tech Rangarajan Dr. Sagunthala R&D Institute of Science & Technology, Chennai — May 2024

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/GAWTHAM0602/final-year-project/blob/main/notebooks/Trojan_Horse_Detection.ipynb)

---

## 👥 Team

| Name | Roll No. | Reg. No. |
|------|----------|----------|
| Sagin Sandoz Fernando E | 20UECS0825 | 16803 |
| K Ajay Kumar Reddy | 20UECS0493 | 15072 |
| Gollapalli Jayanth | 20UECS0339 | 16923 |

**Guide:** Dr. S. Amutha, ME., Ph.D., Associate Professor  
**Department:** Computer Science & Engineering, School of Computing

---

## 📋 Abstract

Deep learning has emerged as a powerful tool for enhancing malware detection and mitigation efforts, offering automated feature extraction capabilities and the potential to detect zero-day malware. This project leverages **Convolutional Neural Networks (CNNs)** and a **Random Forest classifier** to detect and classify Trojan Horse malware from grayscale binary image representations of executable files.

**Keywords:** Deep Learning · Malware Detection · CNN · Random Forest · Trojan Horse · Cybersecurity · IoT

---

## 🚀 Open in Google Colab

Click the badge below to open the complete notebook directly in Google Colab (GPU recommended):

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_GITHUB_USERNAME/trojan-horse-detection/blob/main/notebooks/Trojan_Horse_Detection.ipynb)

> **⚠️ Before running:** Replace `YOUR_GITHUB_USERNAME` above with your actual GitHub username after pushing this repository.

---

## 📁 Repository Structure

```
trojan-horse-detection/
├── notebooks/
│   └── Trojan_Horse_Detection.ipynb   ← Main notebook (all code)
├── docs/
│   └── report_summary.md              ← Project report summary
├── results/
│   └── results_summary.md             ← Results & metrics summary
├── README.md                          ← This file
├── requirements.txt                   ← Python dependencies
└── .gitignore
```

---

## 🏗️ System Architecture

```
Dataset (MalImg)
     │
     ▼
CNN Model (Classification)
     │
     ▼
Classification → Confusion Matrix
     │
     ▼
CNN Model (Detection)
     │
     ├──► Malware Image
     └──► Benign Image
               │
               ▼
         Random Forest Algorithm
               │
               ▼
            Accuracy
```

---

## 📊 Dataset

The **MalImg Dataset** is used — malware binaries converted to 8-bit grayscale images. Each pixel represents one byte of the binary file.

| # | Family | Name | Variants |
|---|--------|------|----------|
| 1 | Trojan | Alueron.gen!J | 198 |
| 2 | Trojan | C2Lop.P | 146 |
| 3 | Trojan | C2Lop.gen!G | 200 |
| 4 | Trojan Downloader | Dontovo.A | 162 |
| 5 | Trojan | Malex.gen!J | 136 |
| 6 | Trojan Downloader | Obfuscator.AD | 142 |
| 7 | Trojan | Skintrim.N | 80 |
| 8 | Trojan Downloader | Swizzor.gen!E | 128 |
| 9 | Trojan Downloader | Swizzor.gen!I | 132 |
| 10 | Trojan Downloader | Wintrim.BX | 97 |

---

## ⚙️ Methodology

### Module 1 — CNN Classification (Keras)
- 25-class malware family classification
- Architecture: `Conv2D → MaxPool → Conv2D → MaxPool → Dropout → Flatten → Dense(128) → Dense(50) → Softmax`
- Input: 64×64 RGB images | Optimizer: Adam | Loss: Categorical Cross-Entropy

### Module 2 — CNN Detection (PyTorch)
- Binary classification: **Benign vs Malware**
- Architecture: 5 convolutional layers (3→16→32→64→128→64 filters) + 3 fully-connected layers
- Input: 256×256 RGB | Optimizer: Adam | Loss: Cross-Entropy

### Step 3 — Random Forest Accuracy Evaluation
- CNN features extracted from conv5 layer
- 100-tree Random Forest trained on extracted features
- Used to determine final detection accuracy

---

## 🛠️ How to Run

### Option A — Google Colab (Recommended)

1. Click the **Open in Colab** badge at the top of this README
2. In Colab: `Runtime → Change runtime type → GPU`
3. Mount your Google Drive and upload the MalImg dataset
4. Run all cells sequentially

### Option B — Local Setup

```bash
# Clone the repository
git clone https://github.com/YOUR_GITHUB_USERNAME/trojan-horse-detection.git
cd trojan-horse-detection

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook notebooks/Trojan_Horse_Detection.ipynb
```

---

## 📦 Requirements

See [`requirements.txt`](requirements.txt) for the full list. Key packages:

- `torch`, `torchvision`
- `tensorflow`, `keras`
- `scikit-learn`
- `matplotlib`, `seaborn`
- `split-folders`, `torchsummary`
- `numpy`, `pandas`

---

## 📈 Results

| Model | Task | Accuracy |
|-------|------|----------|
| Keras CNN | 25-class classification | See notebook output |
| PyTorch CNN | Binary detection | See notebook output |
| Random Forest | Feature-based accuracy | See notebook output |

The **Random Forest + CNN hybrid** outperforms the existing Decision Tree baseline in both accuracy and processing efficiency.

---

## 📚 References

1. Xiaofei Xing et al., "A malware detection approach using autoencoder in deep learning," 2022.
2. Mulhem Ibrahim et al., "A method for automatic android malware detection based on static analysis and deep learning," 2022.
3. Omer Aslan et al., "A new malware classification framework based on deep learning algorithms," 2021.
4. Hanxun et al., "A worm detection system based on deep learning," 2020.
5. Mohammed et al., "An Ensemble-Based parallel Deep Learning Classifier With PSO-BP Optimization For Malware Detection," 2023.
6. Sandeep Gupta et al., "An Investigation Of Cyber-Attacks And Security Mechanisms For Connected And Autonomous Vehicles," 2023.
7. Jeongwoo Kim et al., "Attention-Based Cross-Modal CNN Using Non-Disassembled Files For Malware Classification," 2023.
8. Nguyet Quang Do et al., "Deep Learning for Phishing Detection: Taxonomy, Current Challenges and Future Directions," 2022.
9. Asma A. Al-Hashmi et al., "Deep-Ensemble and Multifaceted Behavioral Malware Variant Detection Model," 2022.
10. Muawia A. Elsadig, "Detection of Denial-of-Service Attack in Wireless Sensor Networks: A Lightweight Machine Learning Approach," 2023.

---

## 📄 License

This project is submitted as an academic major project at Vel Tech R&D Institute of Science & Technology. All rights reserved by the authors.
