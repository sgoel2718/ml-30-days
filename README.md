# ML 30 Days

My 30-day journey through machine learning and AI, from Python basics to transformers, RAG and agents, built alongside the PG Certification in AI/ML at IIIT Hyderabad. Each day has a runnable notebook with concepts, a live demo on real data, and exercises.

- **Plan:** [30-Day ML & AI Mastery Plan (PDF)](docs/30-Day-ML-AI-Mastery-Plan.pdf) · [Markdown version](docs/30-Day-ML-AI-Mastery-Plan.md)
- **Revision:** [`index.html`](index.html) is a sticky-notes board of the key points from each day. Download it and open it in any browser, or view it online if GitHub Pages is enabled.

## Daily notebooks

| Day | Topic | Live demo | Open |
| --- | --- | --- | --- |
| 1 | Python proficiency: types, data structures, comprehensions, functions, classes | Student marks analyzer in core Python | [Notebook](notebooks/Day01_Python_Proficiency.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day01_Python_Proficiency.ipynb) |
| 2 | NumPy, Pandas, Matplotlib, Seaborn, SciPy | Titanic exploratory data analysis | [Notebook](notebooks/Day02_NumPy_Pandas_EDA.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day02_NumPy_Pandas_EDA.ipynb) |

Upcoming: probability (Day 3), statistics (Day 4), linear algebra (Day 5), calculus (Day 6), then classical ML, deep learning, transformers, RAG and deployment. See the plan for the full schedule.

## Running the notebooks

The easiest way is Google Colab: use the Colab links above, where every library used here is pre-installed. If this repository is private, Colab asks once for permission to read your private GitHub repositories.

To run locally:

```bash
pip install numpy pandas matplotlib seaborn scipy scikit-learn jupyter
jupyter notebook
```

## Capstone

Days 31–45 are a capstone project for the IIIT Hyderabad presentation. The recommended choice is a real-time tweet analytics system with an AI insights assistant; the plan lists the alternatives.
