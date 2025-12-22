# 🎬 Sentiment Analysis of Korean Movie Reviews (NSMC)

This project performs **binary sentiment classification (positive vs. negative)** on Korean movie reviews using classical NLP techniques. It focuses on how **linguistic preprocessing and feature extraction** affect sentiment prediction in a **morphologically rich language** such as Korean.
<br/>
<br/>

## 📌 Motivation

Korean sentiment analysis presents several challenges:
- Agglutinative morphology
- Informal and colloquial expressions
- Short, noisy user-generated text

Instead of complex neural architectures, this project adopts an **interpretable and lightweight approach** using TF-IDF–based representations.  
The goal is to understand **which lexical features contribute most strongly to sentiment prediction** in Korean text.
<br/>
<br/>

## 📂 Dataset

**Naver Sentiment Movie Corpus (NSMC)**  
https://github.com/e9t/nsmc/

- Korean-language movie reviews scraped from Naver Movies
- Each review is shorter than **140 characters**
- Balanced binary sentiment labels:
  - **100,000 negative reviews** (ratings 1–4)
  - **100,000 positive reviews** (ratings 9–10)
- Neutral reviews (ratings 5–8) are excluded

The dataset construction follows the methodology described in  
*Maas et al., 2011 – Large Movie Review Dataset*.
<br/>
<br/>

## 🧠 Approach

### 1. Text Preprocessing
- Korean morphological analysis using **KoNLPy**
- Tokenization adapted to Korean grammatical structure
- Stopword filtering and basic normalization
<br/>

### 2. Feature Extraction
- **TF-IDF vectorization** to capture term importance across documents
- Sparse feature representations suitable for short-text classification
<br/>

### 3. Classification
- Supervised learning on TF-IDF features
- **Logistic Regression** classifier for binary sentiment prediction
<br/>
<br/>

## 📊 Analysis & Interpretation

Beyond predictive performance, this project emphasizes **model interpretability** through:
- Visualization of **word-level TF-IDF weights**
- Inspection of terms contributing most strongly to positive and negative predictions
<br/>

This qualitative analysis helps reveal:
- Emotionally salient adjectives and expressions
- Frequency-driven biases in bag-of-words representations
- Limitations of context-free feature extraction for Korean sentiment analysis
<br/>
<br/>

## 📈 Results

- Balanced dataset (50% positive / 50% negative)
- Classification performance above the random baseline (50%)
- Results demonstrate that TF-IDF combined with Logistic Regression provides a strong baseline for Korean sentiment classification

*(Exact metrics may vary depending on preprocessing and training settings.)*
<br/>
<br/>

## ⚠️ Limitations & Future Work

### Limitations
- TF-IDF ignores word order and contextual semantics
- Sarcasm and implicit sentiment are difficult to capture
- Context-aware representations are not considered
<br/>

### Future Work
- Applying contextual models (e.g., Transformer-based encoders)
- Subword-level representations for handling morphological variation
- Error analysis focusing on sarcastic or ambiguous reviews
<br/>
<br/>

## 🛠 Tech Stack

| Category | Tools |
|------|------|
| NLP | KoNLPy, TF-IDF |
| Machine Learning | scikit-learn |
| Visualization | Matplotlib, Seaborn |
| Language | Python |
<br/>
<br/>

## 📚 References

- 머신러닝 네이버 영화 리뷰 감성 분석  
  https://sunnyroad.tistory.com/39
- Naver Movie Review Sentiment Analysis  
  https://wikidocs.net/44249
- Maas et al., 2011. *Learning Word Vectors for Sentiment Analysis*
<br/>
<br/>
