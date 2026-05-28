# MLP Experiment Manager

A neural network experiment manager that trains and evaluates Multi-Layer Perceptron (MLP) models, storing results in a persistent JSON database.

---

## 🚀 Installation

1. Download the `MLP.exe` file from the `dist/MLP` folder  
2. Place it in your desired directory  
3. *(Optional)* Place your CSV datasets in the same folder  

---

## ▶️ Usage

Run `MLP.exe` from the command line or by double-clicking the file.

---

## 🧪 First Run (New Experiment)

```
=== MLP Experiment Manager ===
Results database: experiment_results.json

Enter seed value (or 0 for new experiment): 6
Enter training dataset path: BTC_train.csv
Enter test dataset path: BTC_test.csv

Training started...
Epoch 0: Loss = 0.7874
...
Early stopping at epoch 1909

Results saved under seed: 6
```

---

## 📊 Example Output

```
=== Results ===
Training Metrics:
Accuracy: 85.07%
F1 Score: 0.8477
```

---

## 🔁 Subsequent Runs (Existing Experiment)

```
=== MLP Experiment Manager ===
Results database: experiment_results.json

Enter seed value (or 0 for new experiment): 1

Found existing experiment with seed 1

=== Results ===
Training Metrics:
Accuracy: 89.58%
F1 Score: 0.8953
```

---

## 📥 Input Requirements

- Training/Test datasets must be CSV files with matching formats  
- Seed values:
  - `0` → Creates a new experiment  
  - `>0` → Loads existing experiment (if available)  

---

## 📤 Output Metrics

For each experiment (stored by seed value):

### Training Metrics:
- Accuracy  
- F1 Score  
- Precision  
- Recall  
- Confusion Matrix  

### Test Metrics:
- Accuracy  
- F1 Score  
- Precision  
- Recall  
- Confusion Matrix  

---

## 📁 File Structure

```
project/
├── MLP.exe                 # Main executable
├── experiment_results.json # Results database
├── BTC_train.csv          # Example training data
├── BTC_test.csv           # Example test data
```

---

## ⚠️ Troubleshooting

- If file paths are not found, use absolute paths (e.g. `C:/path/to/file.csv`)  
- Ensure CSV files are properly formatted  
- Check write permissions for `experiment_results.json`  

---

## ⚙️ Performance Notes

- Early stopping implemented (patience = 100)  
- Metrics calculated on both training and test sets  
- Results persist between sessions via JSON database  