# 🤖 GPT-Style Language Model Overview

## 📂 Project Overview
This project implements a **GPT-style character-level language model** using **PyTorch**. It is trained on **Child Speech** and **Shakespeare** datasets to generate coherent text sequences. The project explores different hyperparameter configurations and their impact on model performance.

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

## ⚙️ Hyperparameter Configurations and Results
### **Configuration 1:** (3 Layers, 128 Embedding, 4 Heads, 256 Block Size)
- **Model Size:** 0.643M parameters
- **Final Losses:**
  - Train: 0.3335
  - Validation: 0.3370
  - Child Speech Test Loss: 0.3437
  - Shakespeare Test Loss: 7.2445
- **Generated Sample:** Displays coherent child-like sentences with some noisy patterns.

### **Configuration 2:** (2 Layers, 192 Embedding, 4 Heads, 256 Block Size)
- **Model Size:** 0.963M parameters
- **Final Losses:**
  - Train: 0.3310
  - Validation: 0.3378
  - Child Speech Test Loss: 0.3427
  - Shakespeare Test Loss: 7.0932
- **Generated Sample:** Produces slightly better-structured outputs with improved coherence.

### **Configuration 3:** (4 Layers, 128 Embedding, 2 Heads, 128 Block Size)
- **Model Size:** 0.824M parameters
- **Final Losses:**
  - Train: 0.3464
  - Validation: 0.3490
  - Child Speech Test Loss: 0.3545
  - Shakespeare Test Loss: 7.0026
- **Generated Sample:** Outputs shorter but contextually reasonable sentences.

---

## 💡 With Bias Enabled
### Notable Improvement in Losses for Child Speech Dataset
- **Best Loss:** 0.3411 (Configuration 2 with Bias)
- Shakespeare Loss remained high, showing model struggle with complex patterns.

---

## 🛠️ Technologies Used
- **Language:** Python
- **Framework:** PyTorch
- **Models:** Transformers (GPT-style)
- **Libraries:** NumPy, Matplotlib

---

## 📝 Conclusion
- **Configuration 2** with **Bias** and **192 embeddings** gave the **best results** on the **Child Speech dataset**, achieving a **loss of 0.3411**.
- Shakespeare dataset results remained challenging due to vocabulary size and complexity.
- Increasing embedding dimensions and reducing layers gave the best trade-off between performance and model size.

---

## 💳 Author
**Ujjayant Kadian**  
