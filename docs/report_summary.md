# Project Report Summary

## Title
Enhanced Deep Learning Techniques to Detect Trojan Horse Attack in Cybersecurity

## Institution
Vel Tech Rangarajan Dr. Sagunthala R&D Institute of Science & Technology  
Department of Computer Science & Engineering, School of Computing  
Chennai 600 062, Tamil Nadu, India — May 2024

## Problem Statement
IoT devices face escalating threats from Trojan horse malware. Existing signature-based and classical ML methods are inadequate against zero-day variants and obfuscated binaries.

## Proposed Solution
A hybrid deep learning pipeline:
1. Convert malware binaries → 8-bit grayscale images (MalImg dataset)
2. CNN (Keras) for 25-class malware family classification
3. CNN (PyTorch) for binary benign/malware detection
4. Random Forest on CNN features for final accuracy evaluation

## Existing System Limitations
- Reliance on feature engineering susceptible to evasion
- Limited publicly available benchmark datasets
- Computationally expensive n-gram static analysis
- Packed malware not handled by image methods
- Vanishing gradient problem in RNNs

## Proposed System Advantages
1. Enhanced interpretability via visualization
2. Robust CNN feature extraction (no manual engineering)
3. Comprehensive static + dynamic + image analysis
4. Scalable and real-time deployable
5. Adaptable to zero-day threats

## Standards Used
- Google Colab: ISO/IEC 27001
- Google Drive: ISO/IEC 27001

## Hardware Requirements
- RAM: Minimum 4 GB
- Storage: Minimum 200 GB
- GPU: P100 (Google Colab) or equivalent

## Software Requirements
- Python 3.7+
- PyTorch, TensorFlow/Keras
- Google Colab / Jupyter
- Packages: sklearn, seaborn, matplotlib, cv2, numpy, pandas
