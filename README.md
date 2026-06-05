# UITS CSE 426 — Search Engine Project

A compact, educational search engine built for the UITS CSE 426 class. This repository contains a self-contained notebook implementation that demonstrates core information retrieval concepts, including text preprocessing, inverted index construction, TF–IDF ranking, boolean retrieval, snippet generation, and a simple interactive search interface.

**Key highlights**
- Implements tokenization, stopword removal, and Porter stemming using NLTK.
- Builds an inverted index and computes TF, IDF, and TF–IDF scores.
- Supports Boolean `AND` / `OR` queries and ranked retrieval for multi-word queries.
- Notebook includes demo queries and an interactive search loop suitable for Colab or local execution.

**Repository contents**
- `Online_Courses.csv` — dataset of online course metadata used by the project.
- `Search_Engine_Project.ipynb` — Jupyter/Colab notebook with the full implementation and demonstrations.
- `README.md` — this file.

**Getting started**

1. Requirements
	 - Python 3.8+ (recommended)
	 - pip
	 - Recommended packages: `pandas`, `numpy`, `nltk`

2. Quick setup (local)
	 - Create and activate a virtual environment (optional but recommended):

		 python3 -m venv .venv
		 source .venv/bin/activate

	 - Install packages:

		 pip install pandas numpy nltk

	 - Download NLTK resources (if running the notebook locally):

		 python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords')"

3. Using the notebook
	 - Open `Search_Engine_Project.ipynb` in JupyterLab, Jupyter Notebook, or upload it to Google Colab.
	 - If running in Colab, mount your Google Drive and update `DATASET_PATH` to point to `Online_Courses.csv`.
	 - Run the cells in order. The notebook includes sections to:
		 - Load and inspect the dataset
		 - Clean and preprocess text
		 - Build the inverted index and compute TF / IDF
		 - Run demo queries and an interactive search loop

**How the search works (brief)**
- Preprocessing: lowercase → punctuation removal → tokenization → stopword removal → stemming.
- Index: `inverted_index[term] = { doc_id: term_frequency, ... }`.
- Ranking: TF(term, doc) × IDF(term) summed across query terms to score documents.
- Retrieval: Boolean `AND` / `OR` to produce candidate lists; TF–IDF ranks the candidates.

**Extending the project**
- Add a `requirements.txt` or `environment.yml` for reproducible installs.
- Replace Porter stemming with lemmatization for better term normalization.
- Add pagination, result caching, or a small Flask/FastAPI front-end for web demos.
- Integrate semantic ranking (embeddings) for improved multi-word query handling.

**License & attribution**
This repository is provided for educational purposes. Feel free to reuse and adapt the code for coursework and experimentation; cite course authors and contributions where appropriate.

If you want, I can also generate a `requirements.txt`, add a short demo script, or improve the notebook's README links — tell me which next step you'd like.
