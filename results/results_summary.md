# Results & Discussion

## Module 1 — Keras CNN (25-class Classification)

- **Dataset:** MalImg validation set (64×64 grayscale images)
- **Model:** Sequential CNN with 2 conv layers + dense layers
- **Output:** Confusion matrix with True/Predicted labels per class
- **Classes tested:** Alueron.gen!J, C2LOP.P, Dontovo.A, Malex.gen!J, Obfuscator.AD, Skintrim.N, Swizzor.gen!E/!I, Wintrim.BX, and more

## Module 2 — PyTorch CNN (Binary Detection)

- **Task:** Classify image as Benign or Malware
- **Architecture:** 5-layer CNN (3→16→32→64→128→64) + 3 FC layers
- **Evaluation:** TensorBoard accuracy & loss curves; confusion matrix
- **Metric:** Normalised confusion matrix (precision per class)

## Random Forest Accuracy (Step 5)

- **Input:** CNN conv5 feature maps flattened to 1D vectors
- **Classifier:** RandomForestClassifier (100 trees, random_state=42)
- **Split:** 80% train / 20% test
- **Result:** Reported as `Random Forest Accuracy: X.XXXX`

## Comparison: Existing vs Proposed

| Criterion | Existing (Decision Tree) | Proposed (Random Forest + CNN) |
|-----------|--------------------------|-------------------------------|
| Feature extraction | Manual / n-gram | Automated (CNN layers) |
| Zero-day detection | ❌ Limited | ✅ Supported |
| Accuracy | Lower | Higher |
| Interpretability | High | High (+ visualization) |
| Scalability | Medium | High |
| Real-time | Limited | ✅ Supported |

## Plagiarism Report
- Plagiarised: **0%**
- Unique: **100%**
- Unique Sentences: 5 (100%)
- Report Generated: Apr 14, 2024
