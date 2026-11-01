# ML 30 Days

My 30-day journey through machine learning and AI, from Python basics to transformers, RAG and agents, built alongside the PG Certification in AI/ML at IIIT Hyderabad. Each day has a runnable notebook with concepts, a live demo on real data, and exercises.

- **Plan:** [30-Day ML & AI Mastery Plan (PDF)](docs/30-Day-ML-AI-Mastery-Plan.pdf) · [Markdown version](docs/30-Day-ML-AI-Mastery-Plan.md)
- **Revision:** [`index.html`](index.html) is a revision site with four sections for every day: **sticky notes** (key points), **formulas** (each symbol explained, with a worked example), **detailed notes** (full beginner-friendly explanations) and **interview prep** (questions with a short answer to say and the full explanation). Download it and open it in any browser, or view it online if GitHub Pages is enabled.

## Daily notebooks

| Day | Topic | Live demo | Open |
| --- | --- | --- | --- |
| 1 | Python proficiency: types, data structures, comprehensions, functions, classes | Student marks analyzer in core Python | [Notebook](notebooks/Day01_Python_Proficiency.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day01_Python_Proficiency.ipynb) |
| 2 | NumPy, Pandas, Matplotlib, Seaborn, SciPy | Titanic exploratory data analysis | [Notebook](notebooks/Day02_NumPy_Pandas_EDA.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day02_NumPy_Pandas_EDA.ipynb) |
| 3 | Probability: events, conditional probability, Bayes' theorem, PMF/PDF/CDF, distributions | Naive Bayes spam filter built by hand | [Notebook](notebooks/Day03_Probability.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day03_Probability.ipynb) |
| 3b | Spam filter step by step: every line of Naive Bayes on 4 emails, with all values printed | Hand-checkable spam filter | [Notebook](notebooks/Day03b_Spam_Filter_Step_by_Step.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day03b_Spam_Filter_Step_by_Step.ipynb) |
| 4 | Statistics: centre, spread, skew; normalisation vs standardisation; sampling; Central Limit Theorem; confidence intervals; hypothesis tests; A/B testing | Scaling real features (k-NN 93% → 98%) and a CLT simulation on Titanic fares | [Notebook](notebooks/Day04_Statistics.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day04_Statistics.ipynb) |
| 5 | Linear algebra: vectors, L1/L2/L∞ norms, dot product and cosine similarity, matrices, transformations and determinants, inverse, rank, eigenvectors and PCA | Rotating, scaling and shearing a photo with matrices; PCA on 30 tumour features | [Notebook](notebooks/Day05_Linear_Algebra.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day05_Linear_Algebra.ipynb) |
| 6 | Calculus: derivatives and rules, chain rule, partial derivatives and gradients, convexity, least-squares error, gradient descent (batch and mini-batch), integration | Gradient descent from scratch fitting tip vs bill, plus a 10-feature version on diabetes data | [Notebook](notebooks/Day06_Calculus.ipynb) · [Colab](https://colab.research.google.com/github/sgoel2718/ml-30-days/blob/main/notebooks/Day06_Calculus.ipynb) |

Upcoming: the AI/ML overview and data (Day 7), then classical ML, deep learning, transformers, RAG and deployment. See the plan for the full schedule.

## Projects

Projects built during the course live in their own portfolio repository, [AI-ML-Projects](https://github.com/sgoel2718/AI-ML-Projects):

| Project | What it does |
| --- | --- |
| [**TextPulse**](https://github.com/sgoel2718/AI-ML-Projects/tree/main/textpulse) | Real-time spam detection and tweet sentiment on 1.6M+ messages, with a live FastAPI dashboard |

## Running the notebooks

The easiest way is Google Colab: use the Colab links above, where every library used here is pre-installed. If this repository is private, Colab asks once for permission to read your private GitHub repositories.

To run locally:

```bash
pip install numpy pandas matplotlib seaborn scipy scikit-learn jupyter
jupyter notebook
```

## Capstone

Days 31–45 are a capstone project for the IIIT Hyderabad presentation. The recommended choice is a real-time tweet analytics system with an AI insights assistant; the plan lists the alternatives.
