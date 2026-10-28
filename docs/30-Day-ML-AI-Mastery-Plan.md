# 30-Day ML & AI Mastery Plan

Prepared for Shubham · 28 October 2026

## How this course works

In 30 days at 2–5 hrs/day (about 60–150 hours) you will reach solid working proficiency across the whole curriculum and build one portfolio-grade capstone; true mastery comes from repeating these projects over the following months. Days 1–30 teach every topic in the curriculum, each ending with a runnable demo; the capstone is built from scratch in Days 31–45.

**Daily format** — say "Day N" in chat and I teach that day's lesson:

1. **Concept (30–45 min)** — intuition first, then the math, with diagrams.
2. **Live demo (45–60 min)** — a complete Colab notebook on a real dataset you run cell by cell.
3. **Exercise (30–60 min)** — you modify the demo; I review your code.
4. **Stretch (optional, +1–2 hrs on 5-hr days)** — a deeper variant or paper reading.
5. **Quiz (10 min)** — 5 questions to lock it in.

**Setup (do once, ~30 min)**

- ☐ Google account → Google Colab (colab.research.google.com) — free GPU for Weeks 3–4
- ☐ Local: Python 3.11 + VS Code + `pip install numpy pandas matplotlib seaborn scikit-learn scipy jupyter`
- ☐ Kaggle account (datasets + free GPU notebooks)
- ☐ Hugging Face account (needed from Day 26)
- ☐ GitHub repo `ml-30-days` — commit every day's notebook (this becomes your portfolio)
- ☐ An LLM API key (OpenAI or Groq free tier) before Day 27

**On 2-hour days** do steps 1–3 only; **on 5-hour days** add the stretch and start capstone EDA early from Day 15 onward.

**Your edge:** your C#/.NET, SQL Server and React background maps directly onto Pandas (≈ LINQ + SQL), FastAPI (≈ ASP.NET Core Web API) and the capstone dashboard. I'll draw those parallels as we go.

## Week 1 (Days 1–7): Bridge module — Python, math and data foundations

Week 1 gives you the Python, probability, linear algebra and calculus that every later algorithm is built on, coded rather than memorised.

| Day | Topic | Key concepts | Live demo |
| --- | --- | --- | --- |
| 1 | Python proficiency | Syntax, data types, lists/tuples/dicts/sets, comprehensions, functions, \*args/\*\*kwargs, lambdas, classes, modules | Student-marks analyzer using only core Python |
| 2 | Key libraries | NumPy arrays & broadcasting, Pandas DataFrames, groupby/merge, Matplotlib/Seaborn plots, SciPy overview | Full EDA of the Titanic dataset |
| 3 | Probability | Events: mutually exclusive vs non-exclusive, independent vs dependent; conditional probability, Bayes' theorem; discrete vs continuous random variables; PMF, PDF, CDF; Bernoulli, Binomial, Poisson, Normal | Simulating dice/coins; a Bayes spam filter by hand |
| 4 | Statistics | Mean/median/mode, variance, std, IQR, skew; normalization vs standardization; sampling, Central Limit Theorem, confidence intervals, hypothesis tests | Standardizing real features; CLT simulation |
| 5 | Linear algebra | Vectors, L1/L2/∞ norms, dot product, matrices and operations, inverse, rank, linear dependence/independence, linear transformations, eigenvalues/eigenvectors | Rotating, scaling and shearing an image with matrices |
| 6 | Calculus | Derivatives, chain rule, partial derivatives, gradients, integration (area under PDF), least-squares error | Gradient descent from scratch fitting a line |
| 7 | Overview of AI/ML + data | AI vs ML vs DL, supervised/unsupervised/reinforcement, formulating real-world problems for ML, representing real-world data (tabular, text, image, audio), data processing & visualization, web scraping | Scrape a website → clean → visualize; frame 3 business problems as ML tasks |

**Week 1 checkpoint:** a notebook that loads a raw CSV, cleans it, standardizes it and fits a line with your own gradient descent.

## Week 2 (Days 8–14): Classical machine learning

Week 2 covers the scikit-learn toolkit end to end: you'll train, tune and honestly evaluate every classical algorithm in the curriculum, which is what most industry ML still runs on.

| Day | Topic | Key concepts | Live demo |
| --- | --- | --- | --- |
| 8 | Principles of ML | Train/validation/test split, cross-validation, overfitting vs generalization, bias–variance, k-NN classifier, linear classifier, decision boundaries | k-NN on Iris and Wine; plotting boundaries as k changes |
| 9 | Regression & classification | Linear regression (normal equation vs GD), Ridge/Lasso, logistic regression, performance metrics: MAE, RMSE, R², confusion matrix, precision, recall, F1, ROC-AUC, PR curves | House-price regression; bank term-deposit classifier |
| 10 | Features | Feature extraction, normalization, transformation (log, Box-Cox), encoding, missing values, imbalance (SMOTE, class weights), feature selection (filter, wrapper, embedded), sklearn Pipelines | Leak-free pipeline that lifts a baseline's F1 |
| 11 | Ensembles | Decision trees (Gini, entropy), sampling: bootstrap & bagging, bagging classifier, voting classifier, Random Forest, AdaBoost, Gradient Boosting, XGBoost, feature importance, SHAP | Employee attrition prediction, 6 models compared |
| 12 | SVM & MLP | Separability vs non-separability, max-margin, soft margin, kernel trick (linear, poly, RBF), MLP classifier & regressor, hyperparameter tuning (GridSearch, Optuna) | SVM kernels on non-linear data; sklearn MLP vs SVM |
| 13 | Unsupervised learning | k-Means, elbow & silhouette, hierarchical clustering & dendrograms, DBSCAN, Gaussian Mixtures | RFM customer segmentation for retail marketing |
| 14 | Dimensionality reduction | PCA (from eigenvectors), simple PCA, PCA EigenFaces, manifold learning, ISOMAP, t-SNE, UMAP | EigenFaces face reconstruction; t-SNE of MNIST digits |

**Week 2 checkpoint:** an end-to-end Kaggle-style notebook (EDA → pipeline → 5 models → tuned ensemble → metrics report) on the bank-marketing dataset.

## Week 3 (Days 15–21): NLP foundations, neural networks and computer vision

Week 3 moves from hand-built features to learned ones: you'll write backpropagation yourself once, then use PyTorch and Keras to build image models that run on video. Switch Colab to a GPU runtime from Day 17.

| Day | Topic | Key concepts | Live demo |
| --- | --- | --- | --- |
| 15 | Representing text & language | NLTK: tokenization, stemming, lemmatization, stopwords, POS, NER; Bag-of-Words, n-grams, TF-IDF, word2vec/GloVe embeddings; text classification, text generation (n-gram), sentiment analysis | Tweet sentiment classifier with TF-IDF + logistic regression |
| 16 | Neural networks from scratch | Perceptron, why XOR needs non-linear solutions, multi-layer perceptron, activations, loss functions, gradient descent (batch, SGD, mini-batch, momentum, Adam), backpropagation | 2-layer network in pure NumPy solving XOR and moons |
| 17 | PyTorch, TensorFlow & Keras | Tensors, autograd, Dataset/DataLoader, training loop; Keras Sequential & functional API; dropout, batch norm, early stopping, weight decay to avoid overfitting | Same MNIST model in PyTorch and Keras, side by side |
| 18 | CNNs | Convolution, filters, stride, padding, pooling, feature maps, appreciating CNNs (what each layer sees), features for perception, image augmentation | CIFAR-10 CNN + filter/activation visualisation |
| 19 | Beyond AlexNet & transfer learning | AlexNet → VGG → Inception → ResNet → EfficientNet → Vision Transformer; transfer learning vs fine-tuning, freezing layers, learning-rate schedules | Food image classifier with ResNet50; emotion recognition from faces (FER-2013) |
| 20 | Computer vision | Image classification vs object detection (YOLO, IoU, NMS, mAP) vs segmentation (semantic: U-Net; instance: Mask R-CNN; SAM), OpenCV, video processing | YOLO detecting objects in a live webcam/video; U-Net food segmentation |
| 21 | Autoencoders & Siamese networks | Autoencoders, denoising AE, reconstruction of images, latent space, anomaly detection via reconstruction error, variational AE, Siamese networks, contrastive & triplet loss | Denoising MNIST; bearing-vibration anomaly detector; face-similarity Siamese net |

**Week 3 checkpoint:** a fine-tuned image classifier above 85% accuracy, with Grad-CAM heat-maps showing what it looks at.

## Days 22–30: Sequences, generative AI, transformers, LLMs, RAG, agents and deployment

The final nine days take you from sequence models to shipping an LLM-powered app behind a FastAPI endpoint — the stack most AI job descriptions ask for in 2026.

| Day | Topic | Key concepts | Live demo |
| --- | --- | --- | --- |
| 22 | RNN, LSTM & GRU | Sequence modelling, vanishing gradients, LSTM gates, GRU, bidirectional RNNs, time-series applications: windowing, stationarity, ARIMA baseline vs LSTM, walk-forward validation | Stock price and daily logistics demand forecasting |
| 23 | Speech & ML in speech/NLP | Audio as signals, spectrograms, MFCCs, features for speech perception, speech emotion recognition, speech-to-text with Whisper | Emotion recognition from speech (RAVDESS); Whisper transcription |
| 24 | GANs & generative models | Generator vs discriminator, DCGAN, mode collapse, conditional GAN, SRGAN for image super-resolution, intro to diffusion models (Stable Diffusion) | DCGAN generating faces/digits; SRGAN upscaling |
| 25 | Attention & Transformers | Seq2seq + attention, self-attention, multi-head attention, positional encoding, encoder vs decoder; BERT, GPT, T5 architectures | Build a mini-transformer in PyTorch; visualise attention |
| 26 | Hugging Face & fine-tuning | Transformers library, pipelines, tokenizers, Datasets, Trainer; fine-tuning BERT (classification, Quora question pairs), fine-tuning GPT-2; LoRA/PEFT, QLoRA | Fine-tune BERT for sentiment; LoRA on a small GPT |
| 27 | LLMs, RAG & LangChain | OpenAI API (ChatGPT), Llama via Ollama, prompt engineering, embeddings, vector databases (FAISS/Chroma), chunking, retrieval, LangChain RAG chains, evaluation | Chat-with-your-PDFs RAG app |
| 28 | Agentic AI & human-in-the-loop | Tool/function calling, ReAct, LangGraph agents, memory, multi-agent patterns, MCP, human-in-the-loop approvals, guardrails | Research agent that searches, summarises and asks for approval before acting |
| 29 | Deployment & practical issues | FastAPI model serving, Docker, Streamlit/Gradio UIs, model compression (quantization, pruning, knowledge distillation, ONNX), data drift, monitoring, MLflow, deployment on Azure / Hugging Face Spaces | Deploy Day 26's BERT model as a FastAPI + Docker API; quantize it 4× smaller |
| 30 | Recommenders, optimal routes & capstone kickoff | Content-based vs collaborative filtering, matrix factorization, neural CF; finding the optimal route (Dijkstra, A\*, vehicle routing with OR-Tools); capstone selection and problem statement | MovieLens recommender; delivery-route optimiser |

**Industry lectures (weekends, ~1 hr each):** Andrej Karpathy's *Neural Networks: Zero to Hero*, 3Blue1Brown's neural-network series, and Stanford CS231n / CS224n lectures on the topics you just covered.

## Capstone (Days 31–45): Real-time Tweet Analytics with an AI insights assistant

Recommended pick: **Real-time system for Tweet Analytics**, because it alone exercises classical ML, deep learning, transformers, RAG, agents and full-stack deployment — and your React/.NET/Azure experience makes the live dashboard a standout in the IIIT Hyderabad demo. Final choice is made on Day 30; the shortlist below are strong alternatives.

**What it does:** ingests a live stream of posts, classifies sentiment and emotion, extracts topics and entities, detects trending spikes, and lets a user ask questions like "Why did sentiment on #budget drop this afternoon?" answered by a RAG assistant over the stream.

**Pipeline**

1. **Ingest** — X's API is paid, so stream either the free Bluesky firehose or a replayed Kaggle tweet dataset (Sentiment140 / TweetEval) through a Python producer → queue.
2. **Process** — clean with NLTK/regex; baseline TF-IDF + logistic regression vs fine-tuned BERTweet/RoBERTa for sentiment and emotion; spaCy NER; BERTopic clustering.
3. **Detect** — rolling-window volume and sentiment; anomaly detection flags trending spikes.
4. **Store** — SQLite/Postgres for metrics; Chroma vector DB for post embeddings.
5. **Ask** — LangChain RAG assistant (Llama or OpenAI) that retrieves relevant posts and explains trends, with an agent that can query metrics.
6. **Serve** — FastAPI backend + React (or Streamlit) live dashboard, Dockerised, deployed to Azure or Hugging Face Spaces.

**Build timeline (2–3 hrs/day)**

| Days | Phase | Output |
| --- | --- | --- |
| 31–32 | Problem statement, data source, EDA | Proposal doc + EDA notebook |
| 33–35 | Baselines and BERT fine-tuning | Model comparison table (accuracy, F1, latency) |
| 36–37 | Streaming pipeline + topic/trend detection | Working end-to-end stream |
| 38–40 | RAG assistant + FastAPI | Q&A endpoint with cited posts |
| 41–42 | Dashboard, Docker, deployment | Live public URL |
| 43–45 | Report, slides, demo video, rehearsal | Submission package |

**Submission package**

- ☐ GitHub repo with README (setup, architecture diagram, results, screenshots)
- ☐ Project report: problem, data, EDA, methods, experiments, results, limitations, ethics, future work
- ☐ 12–15 slide presentation for the IIIT Hyderabad panel
- ☐ 3-minute demo video + live demo
- ☐ Viva prep: 30 likely panel questions with answers

**Strong alternatives**

| Project | What it showcases | Difficulty |
| --- | --- | --- |
| Quora question pairs with same intent | Siamese networks, BERT fine-tuning, embeddings | Medium |
| Talent retention & attrition prediction | Tabular ML, XGBoost, SHAP explainability + an HR GenAI assistant | Low–medium (safest) |
| Food image segmentation | U-Net, SAM, transfer learning, augmentation | Medium–high |
| Image super-resolution with GAN | SRGAN, perceptual loss, PSNR/SSIM | High (GPU-heavy) |
| Daily demand forecasting for logistics | Time series, LSTM vs gradient boosting, route optimisation | Medium |

## Curriculum coverage map

Every item in your IIIT Hyderabad syllabus is mapped to a day below; extras I added are listed last.

| Syllabus area | Items | Day(s) |
| --- | --- | --- |
| Bridge: Python | Basics, data types & structures, functions, library packages | 1–2 |
| Bridge: Probability & statistics | Continuous/discrete RVs, mutually exclusive & independent events, PDF, CDF, centre & spread, normalization & standardization | 3–4 |
| Bridge: Calculus & linear algebra | Vectors, norms, matrices & operations, linear (in)dependence, linear transformations, least-square error, derivatives, chain rule, integration, gradients | 5–6 |
| Module 1 | NumPy/SciPy/Pandas/Matplotlib, AI/ML overview, principles of ML, data processing & visualization, feature selection & extraction, simple algorithms, classification & regression, dimensionality reduction, text representation, bootstrap & bagging, problem formulation, real-world data, manifold & unsupervised learning, overfitting & generalization, performance metrics | 2, 7–15 |
| Module 2 | Problem formulation, non-linear solutions & MLP, gradient descent & backprop, PCA EigenFaces, SVM & kernels, NLP, features for perception, ensembles (RF, AdaBoost) | 7, 11–16, 18, 23 |
| Module 3 | Intro to DL, PyTorch/TensorFlow/Keras, CNNs, autoencoders, RNN/LSTM/GRU, time series, recommendation systems, beyond AlexNet & transfer learning, FastAPI, deployment, model compression, Siamese networks & GANs, computer vision, speech & NLP, attention & transformers (BERT, GPT, T5), Hugging Face, fine-tuning BERT & GPT, LLMs (OpenAI API, Llama), RAG & LangChain, human-in-the-loop & agentic AI | 16–30 |
| Module 4 / experiential | Web scraping & NLTK, k-NN, linear classifier, decision tree, bagging & voting classifiers, linear & logistic regression, PCA, ISOMAP, t-SNE, k-Means & hierarchical, XGBoost, reconstruction of images, sentiment analysis, emotion recognition from face & speech, optimal route, image augmentation/segmentation/classification, object detection, video processing | 7–15, 18–23, 30 |
| Extras added | Cross-validation & tuning (Optuna), SHAP explainability, class imbalance, Grad-CAM, Vision Transformers, diffusion models, LoRA/QLoRA, vector databases, LangGraph & MCP, Docker, MLflow, data drift | Throughout |
