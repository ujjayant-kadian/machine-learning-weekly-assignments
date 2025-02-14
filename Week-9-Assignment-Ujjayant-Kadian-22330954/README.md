# 🤖 GPT-Style Language Model Overview

## 📂 Project Overview
This project implements a **GPT-style character-level language model** using **PyTorch**, trained on **Child Speech** and **Shakespeare** datasets. It generates text sequences and compares performance across different model configurations.

---

## 📝 Datasets Summary
### 📊 Child Speech Dataset
- **Training Set:**
  - Character-level Vocabulary Size: 40
  - Word-level Vocabulary Size: 88
  - Total Words: 55,076
- **Test Set:**
  - Character-level Vocabulary Size: 40
  - Word-level Vocabulary Size: 88
  - Total Words: 5,347

### 📖 Shakespeare Dataset
- Character-level Vocabulary Size: 65
- Word-level Vocabulary Size: 25,670
- Total Words: 202,651

---

## 🚀 How to Use This Project

### 1️⃣ **Clone the Repository**
Make sure you have Git installed. Run:
```bash
git clone https://github.com/yourusername/gpt-language-model.git
cd gpt-language-model
```

### 2️⃣ **Install Dependencies**
Ensure `Python 3.9+` is installed. Install required libraries:
```bash
pip install torch matplotlib numpy
```

### 3️⃣ **Train the Model**
You can run the model using different configurations. Open the file `gpt.py` and set your preferred hyperparameters.

To train with default settings:
```bash
python gpt.py
```

- The model will print losses at intervals and save the best model to `best_model.pth`.
- It will generate text using the trained model.
- If you want to retrain, delete existing `best_model.pth` model and re-run the above command.
- To modify hyperparameters, edit the following section in the code:
```python
batch_size = 64
block_size = 256
max_iters = 2000
learning_rate = 3e-4
n_embd = 192
n_head = 4
n_layer = 2
dropout = 0.2
```

## ⚙️ Hyperparameter Configurations and Results

### **Configuration 1:** (3 Layers, 128 Embedding, 4 Heads, 256 Block Size)
- **Model Size:** 0.643M parameters
- **Best Losses:** Train: 0.3335 | Validation: 0.3370
- **Child Speech Test Loss:** 0.3437  
- **Shakespeare Test Loss:** 7.2445  

### **Configuration 2:** (2 Layers, 192 Embedding, 4 Heads, 256 Block Size) – **Best Performance**
- **Model Size:** 0.963M parameters
- **Best Losses:** Train: 0.3310 | Validation: 0.3378
- **Child Speech Test Loss:** 0.3427  
- **Shakespeare Test Loss:** 7.0932  

### **Configuration 3:** (4 Layers, 128 Embedding, 2 Heads, 128 Block Size)
- **Model Size:** 0.824M parameters
- **Best Losses:** Train: 0.3464 | Validation: 0.3490
- **Child Speech Test Loss:** 0.3545  
- **Shakespeare Test Loss:** 7.0026  

---

## 💡 With Bias Enabled
### Performance Observation
- **Best Child Speech Test Loss:** 0.3411 (Configuration 2 with Bias)
- Shakespeare Loss remained high, indicating complexity challenges.

---

## 📊 Sample Generated Outputs

**When trained on Child Speech Dataset:**
```
No touch I jump Daddy read me dinosaur book before bed
Uh oh spill More more
I jump Look airplane
Look moon Loook moon
```
---

## 🛠️ Technologies Used
- **Language:** Python
- **Framework:** PyTorch  
- **Libraries:** NumPy, Matplotlib  
- **Model:** GPT-style Transformer  

---

## 📝 Conclusion
- **Best Configuration:** **2 Layers, 192 Embedding, 4 Heads, Bias Enabled**  
  - Achieved the lowest loss on the **Child Speech dataset**.  
- The **Shakespeare dataset** was more complex due to its larger vocabulary.  
- Increasing embeddings with fewer layers was the most efficient.  

---

## 💳 Author
**Ujjayant Kadian**  
