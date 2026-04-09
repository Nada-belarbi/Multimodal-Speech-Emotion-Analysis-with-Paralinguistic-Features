# 🎧 Speech Emotion Recognition under Speaker-Independent Evaluation  
## Paralinguistic Feature-Based Analysis (RAVDESS)

---

## 📌 Overview

This project presents a research-oriented study on **speech emotion recognition (SER)** using the RAVDESS dataset.

The objective is to investigate how **paralinguistic acoustic features** can be used to classify emotional states, with a strong focus on a critical methodological challenge:

👉 **generalization across unseen speakers**

Rather than optimizing performance alone, this work emphasizes:
- rigorous experimental design,
- evaluation protocol validity,
- and critical interpretation of results.

---

## 🎯 Objectives

- Build an end-to-end pipeline for speech emotion recognition  
- Extract meaningful **acoustic and paralinguistic features**  
- Evaluate models under **speaker-independent conditions**  
- Analyze classification errors and generalization limitations  
- Investigate how speech signals encode emotional information beyond lexical content  

---

## 📊 Dataset

This project uses the **RAVDESS dataset** (Ryerson Audio-Visual Database of Emotional Speech and Song), a standard benchmark in speech emotion recognition.

Main characteristics:
- 24 speakers (actors)
- 8 emotional classes
- High-quality controlled recordings
- Balanced dataset (with slight class imbalance)

---

## ⚙️ Methodology

### 1. Data Processing
- Audio loading and preprocessing  
- Label extraction from filenames  
- Speaker identification and grouping  

---

### 2. Feature Extraction

The model relies on **handcrafted paralinguistic features**:

- MFCC (Mel-Frequency Cepstral Coefficients)  
- Spectral centroid  
- Zero-crossing rate  
- Chroma features  
- Energy (RMS statistics)  

These features capture key acoustic properties such as:
- tone,
- intensity,
- rhythm,
- spectral distribution.

---

### 3. Experimental Design ⭐

A central contribution of this project is the comparison between two evaluation protocols:

- **Standard stratified split** (sample-level)
- **Speaker-independent split (actor-disjoint)**

The second approach ensures a **realistic evaluation setting**, preventing the model from exploiting speaker-specific patterns.

👉 This highlights a key issue in speech ML:  
**performance can be significantly overestimated when speaker overlap exists between train and test sets.**

---

### 4. Models

We evaluate classical machine learning models:

- Random Forest (baseline)
- Multi-Layer Perceptron (MLP)

The goal is to:
- assess the discriminative power of acoustic features  
- compare model capacity  
- analyze robustness under realistic conditions  

---

## 📈 Results

Performance is evaluated using:
- Accuracy  
- Balanced accuracy  
- Precision / Recall / F1-score  
- Confusion matrix  

### Key Findings

- **~92% accuracy** with standard split  
- **~48% accuracy** with speaker-independent split  

👉 This reveals a **~44% performance drop**, demonstrating:

- strong **speaker dependency**
- difficulty of **cross-speaker generalization**
- importance of proper evaluation protocols  

Despite this, results remain significantly above random baseline (12.5%), confirming that acoustic features carry meaningful emotional information.

---

## 🔍 Error Analysis

The project includes detailed error analysis:

- Identification of **frequently confused emotion pairs**  
- Strong variability across emotion classes  
- Detection of **systematic confusion patterns** (e.g., happy vs sad)  
- Analysis of **generalization gap (overfitting to speakers)**  

---

## 🧠 Key Insights

- Speech encodes rich **paralinguistic information** beyond words  
- Models tend to learn **speaker-specific patterns** instead of emotion  
- Proper evaluation is **crucial in speech-related tasks**  
- Emotion recognition from audio alone remains **intrinsically difficult**  

---

## 🔬 Research Perspective

This project connects to broader research directions:

- speaker-invariant representation learning  
- robust speech understanding  
- paralinguistic signal modeling  
- limitations of handcrafted acoustic features  

---

## 🚀 Future Work

- Use **pretrained audio embeddings** (wav2vec, HuBERT)  
- Explore **deep learning architectures** (CNN, Transformers)  
- Integrate **textual information (ASR + NLP)**  
- Extend toward **multimodal learning (audio + text)**  
- Improve robustness in real-world noisy environments  

---

## 🛠️ Tech Stack

- Python  
- Librosa  
- Scikit-learn  
- NumPy / Pandas  
- Matplotlib / Seaborn  

---


---

## 👩‍💻 Author

**Nada Belarbi**  
AI & Machine Learning Engineering Student  

- Focus: Machine Learning, Speech Processing  
- Interests: Speech understanding, representation learning, AI systems  

---

## ✨ Relevance

This work addresses a key question in speech AI:

> Not only *what is said*, but *how well models generalize across speakers*.

It highlights a critical gap between **apparent performance** and **real-world robustness** in speech emotion recognition systems.
