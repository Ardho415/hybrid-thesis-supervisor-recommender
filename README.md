# 🎓 Hybrid Semantic Recommendation System for Thesis Supervisor Assignment

A hybrid recommendation system that recommends thesis proposal supervisors by combining **Semantic Content-Based Filtering (CBF)** and **Collaborative Filtering (CF)**. The system leverages **Sentence-BERT (SBERT)** embeddings and **TF-IDF** representations to understand thesis topics semantically while utilizing historical supervision data to improve recommendation quality.

## 🚀 Features

- Semantic similarity using Sentence-BERT (SBERT)
- TF-IDF based text representation
- Hybrid Content-Based Filtering (SBERT + TF-IDF)
- Collaborative Filtering using historical supervision records
- Hybrid scoring between CBF and CF
- Automatic hyperparameter tuning
- Cold-start handling for new lecturers
- Performance evaluation using:
  - Precision@K
  - Recall@K
  - Hit Rate@K
  - Mean Reciprocal Rank (MRR)

---

## 📂 Project Structure

```
.
├── Projek_Akhir_KSIK.ipynb
├── data_historis.csv
├── data_test.csv
├── data_dosen.csv
└── README.md
```

---

## 🧠 Methodology

The recommendation pipeline consists of several stages:

1. **Data Loading**
   - Historical thesis-supervisor assignments
   - Student thesis proposals
   - Lecturer profiles

2. **Semantic Embedding**
   - Encode thesis titles using Sentence-BERT
   - Encode lecturer expertise using combined concentration fields and keywords

3. **Content-Based Filtering**
   - Compute semantic similarity using SBERT
   - Compute lexical similarity using TF-IDF
   - Fuse both similarity scores

4. **Collaborative Filtering**
   - Compare new thesis proposals with historical thesis data
   - Aggregate lecturer scores using:
     - supervision role weighting
     - recency weighting

5. **Hybrid Recommendation**
   - Combine CBF and CF scores

   Final score:

   ```
   Final Score = α × CBF + (1 − α) × CF
   ```

6. **Hyperparameter Tuning**
   - Alpha
   - Beta
   - Top-N historical documents
   - Recency decay
   - Secondary supervisor weight

7. **Evaluation**
   - Precision@K
   - Recall@K
   - Hit Rate@K
   - Mean Reciprocal Rank (MRR)

---

## 🛠 Technologies

- Python
- Pandas
- NumPy
- Sentence-Transformers (SBERT)
- Scikit-learn
- SciPy
- Jupyter Notebook

---

## 📊 Recommendation Approach

The system combines semantic understanding and historical supervision patterns.

### Content-Based Filtering

- Sentence-BERT Embedding
- TF-IDF
- Cosine Similarity

### Collaborative Filtering

- Historical thesis similarity
- Lecturer supervision history
- Role weighting
- Time decay weighting

### Hybrid Model

The final recommendation is obtained by combining both approaches, allowing the system to perform well even for lecturers with limited supervision history.

---

## 📈 Evaluation Metrics

The recommendation quality is evaluated using:

- Precision@K
- Recall@K
- Hit Rate@K
- Mean Reciprocal Rank (MRR)

The notebook also compares:

- TF-IDF Baseline
- CBF Only
- CF Only
- Hybrid Recommendation

---

## 💡 Future Improvements

- Deploy as a web application
- Integrate lecturer availability and workload
- Support multilingual thesis titles
- Incorporate Large Language Models (LLMs) for semantic profiling
- Real-time recommendation API

---

## 👥 Authors

- Ardho Firdaus
- Team Project — Final Project KSIK
