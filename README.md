# 🇮🇩 Indonesian Spelling Corrector using RNN

This repository contains an implementation of a **character-level spelling correction system** for Indonesian words using a Sequence-to-Sequence **Recurrent Neural Network (RNN)** architecture. The model is trained on a curated dataset of correct root words and learns to map noisy or misspelled inputs into their proper forms.

---

## 📁 Repository Structure

```
📦 Indonesian_Spelling_Corrector
├── spelling_corrector.ipynb     # Main notebook: preprocessing, training, evaluation
├── root_word.txt                # Dataset of 41,000+ root words
├── char_utils.py                # Character-index conversion utils
├── trained_model.h5             # Saved RNN model (optional, after training)
```

---

## 📌 Key Features

- 🔡 Character-level sequence-to-sequence LSTM architecture
- ⚙️ Preprocessing includes cleaning, gibberish generation, and one-hot encoding
- 📈 Exploratory Data Analysis (EDA) for character, prefix, suffix, and length distribution
- 🧪 Model trained using categorical crossentropy loss and RMSprop optimizer
- 📚 Easy to extend for online spelling correction or auto-completion

---

## 🛠 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Indonesian_Spelling_Corrector.git
   cd Indonesian_Spelling_Corrector
   ```

2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn plotly tensorflow
   ```

3. Open and run the notebook:
   ```bash
   jupyter notebook spelling_corrector.ipynb
   ```

---

## 📊 Dataset

The dataset `root_word.txt` contains more than 41,000 valid Indonesian root words. Synthetic misspellings are generated via a gibberish function that performs random insertions, deletions, and substitutions to simulate real-world typos.

---

## 🧠 Model Architecture

- **Encoder**: LSTM layer that processes the noisy input sequence
- **Decoder**: LSTM layer that outputs the corrected word sequence
- **Activation**: Softmax on decoder output
- **Loss Function**: Categorical crossentropy
- **Evaluation**: Accuracy, sequence comparison

---

## 📈 EDA Insights

The notebook includes EDA visualizations such as:
- Distribution of word lengths
- Top prefixes and suffixes in root words
- Frequency of individual characters
- Word structure insights via scatter plots

---

## ✨ Example

**Input (misspelled):** `kmpiter`  
**Output (corrected):** `komputer`

---

## 📬 Contact

**Alexander Tiopan**  
📧 alexandertiopan1212@gmail.com  
🌐 [GitHub](https://github.com/alexandertiopan1212)  
🌐 [LinkedIn](https://www.linkedin.com/in/alexander-tiopan/)

---

## 📝 License

This project is licensed under the MIT License — feel free to use, modify, and build upon it with attribution.
