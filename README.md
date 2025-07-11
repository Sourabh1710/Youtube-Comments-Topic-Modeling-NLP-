# 🧠 Python Project - Topic Modeling on YouTube Comments (NLP)

![Python](https://img.shields.io/badge/python-3.10-blue)
![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange)

This project performs **Topic Modeling using NLP techniques** on real YouTube comments using the YouTube Data API v3. It extracts top comments from videos on a specific topic (e.g., "Tech Reviews") and uncovers dominant themes discussed by the audience.


---

## 📌 Business Problem

Understand what topics customers or viewers care about most by analyzing large volumes of unstructured comments — useful for:
- Influencers
- Marketing teams
- Product strategy & feature planning

---

## 🚀 Tools Used

- Python 3.10
- pandas, matplotlib, wordcloud, nltk, gensim, pyLDAvis
- YouTube Data API v3
- Jupyter Notebook

---

## 🔍 Project Pipeline

### 🔹 Step 1: Data Collection via API
- Pulled top 500 comments each from multiple videos using the YouTube API.
- Topic of focus: `"Tech Reviews"` (e.g., Samsung vs iPhone, Microsoft Copilot, etc.)

### 🔹 Step 2: Text Preprocessing
- Lowercasing, removing links & special characters
- Tokenization using `nltk`
- Stopwords removal

### 🔹 Step 3: Topic Modeling with Gensim's LDA
- Created dictionary & corpus
- Trained LDA model on comment tokens
- Extracted 8 topics with top keywords

### 🔹 Step 4: Visualizations
- WordClouds per topic
- pyLDAvis interactive chart
- Saved all charts in the `charts/` folder

---

## 📂 Project Structure
<pre>
youtube-nlp-topic-modeling/
├── data/ ← Raw CSV data (YouTube comments)
├── charts/ ← Wordclouds + pyLDAvis HTML
├── lda_model/ ← Dictionary & corpus files
├── notebooks/
│ └── topic_modeling_youtube_comments.ipynb
├── requirements.txt
└── README.md
</pre>

---

## 📸 Charts & Visuals

All visual outputs are saved in the `/charts` folder:
- 🔸 `topic_0.png` to `topic_7.png` (wordclouds)
- 🔸 `topic_model_visualization.html` (interactive visualization)

---

## ✅ Key Findings

| Topic | Example Keywords                     | Theme                              |
|-------|--------------------------------------|-------------------------------------|
| 0     | fireship, illusion, watching         | Channel-specific reactions          |
| 2     | video, like, time, would             | Viewer appreciation / tone          |
| 4     | copilot, microsoft, code, github     | Dev tool buzz (Microsoft Copilot)   |
| 3     | iphone, samsung, camera, ultra       | Tech comparisons                    |

---

## 🧠 Takeaways

- Viewers talk about specific tools like **Copilot**, **OpenAI**, **Samsung/Apple**.
- Some topics cluster around **emotions** (e.g., “love”, “wow”, “bro”) — others are **tech-driven**.
- Perfect case for understanding **audience interests** via unsupervised NLP.

---

## 📦 Installation

```bash
git clone https://github.com/YourName/youtube-nlp-topic-modeling.git
cd youtube-nlp-topic-modeling
python -m venv venv
.\venv\Scripts\activate     # Windows
pip install -r requirements.txt
jupyter notebook
```

## 👨‍💼 Author

**Sourabh Sonker**  
**Aspiring Data Scientist**

---
