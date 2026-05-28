# Machine Learning Projects

A collection of applied machine learning notebooks produced as coursework for B.S. Data Science and Analytics at the University of Santo Tomas. Each notebook addresses a distinct problem domain and methodology, applied to real-world datasets including Philippine election data, IMDB reviews, Telco Churn records, and U.S. Census income data.

---

## Notebooks

### Boosting and Ensemble Methods
**File:** [Boosting and Ensemble.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Boosting%20and%20Ensemble.ipynb)

Compares bagging (Random Forest) against boosting algorithms (AdaBoost, Gradient Boosting) on a financial classification task. Demonstrates that tree-based ensembles outperform traditional econometric approaches like Logistic Regression by capturing non-linear feature interactions, achieving over 86% accuracy. Analyzes how boosting models disproportionately focus on high-signal financial indicators (e.g., capital gains) through iterative error correction, rather than distributing weight across general demographic traits.

**Methods:** Random Forest, AdaBoost, Gradient Boosting, Logistic Regression
**Key result:** Boosting ensembles exceed 86% accuracy; outperform linear baselines on non-linear financial data

---

### Dimensionality Reduction
**File:** [Dimensionality Reduction.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Dimensionality%20Reduction.ipynb)

Applies PCA, t-SNE, and UMAP to the Countries of the World 2023 dataset, analyzing development indicators including GDP, Birth Rate, and Infant Mortality. Evaluates the interpretability and visualization trade-offs of each technique. Concludes that PCA is best suited for explanation and reporting due to its linear, interpretable components, while t-SNE and UMAP are superior for discovering clusters and handling complex, non-linear, or overlapping data structures.

**Methods:** PCA, t-SNE, UMAP
**Dataset:** Countries of the World 2023
**Key result:** PCA favored for reporting; t-SNE and UMAP favored for cluster discovery and non-linear visualization

---

### Imbalance Identification
**File:** [Imbalance Identification.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Imbalance%20Identification.ipynb)

Diagnoses and addresses class imbalance in the Telco Churn dataset. Through systematic evaluation of multiple diagnostic approaches, determines that the core issue is threshold calibration and prior skew rather than insufficient feature informativeness or sheer minority-class scarcity. Recommends and validates the `class_weight='balanced'` parameter, which upweights minority-class errors during training and significantly improves recall without degrading the model's underlying discrimination ability.

**Methods:** Logistic Regression, Class Weight Balancing, Threshold Calibration, ROC/PR Analysis
**Dataset:** Telco Customer Churn
**Key result:** `class_weight='balanced'` recovers recall on the minority class without meaningful AUC loss

---

### Market Basket Analysis
**File:** [Market Basket Analysis.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Market%20Basket%20Analysis.ipynb)

Applies the Apriori algorithm to discover association rules in ticket-voting behavior during the 2022 Philippine national elections, using province-level voting data as transaction records. Captures the dominance of the UniTeam coalition across regional blocs, driven by political endorsements and coordinated slate voting. Critically evaluates the limitations of province-level aggregation and argues that municipality-level analysis would surface finer regional subcultures and hidden minority voting patterns obscured by aggregation.

**Methods:** Apriori Algorithm, Association Rule Mining, Support/Confidence/Lift metrics
**Dataset:** 2022 Philippine National Elections (province-level)
**Key result:** Association rules reflect UniTeam coalition dominance; province-level aggregation masks subnational heterogeneity

---

### Natural Language Processing
**File:** [Natural Language Processing.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Natural%20Language%20Processing.ipynb)

Builds an end-to-end NLP pipeline for sentiment analysis on movie reviews. Directly benchmarks NLTK's Porter Stemmer against spaCy's Lemmatizer, applies custom stop-word filtering to reduce noise, and vectorizes cleaned text into a TF-IDF matrix for feature extraction. Evaluates relationships between positive and negative reviews using a Cosine Similarity matrix to identify linguistic overlap and divergence across sentiment classes.

**Methods:** Porter Stemming, spaCy Lemmatization, TF-IDF Vectorization, Cosine Similarity
**Dataset:** Movie reviews (labeled sentiment)
**Key result:** TF-IDF with lemmatization and custom stop-word filtering produces cleaner sentiment signal than stemming alone

---

### Regularization and Advanced Classification
**File:** [Regularization.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Regularization.ipynb)

Evaluates ten machine learning models on the task of predicting whether an individual earns over $50,000 annually, using U.S. Census demographic and employment data. Benchmarks Linear Probability Models and regularized Logistic Regressions (L1, L2) against tree-based algorithms. Gradient Boosting emerges as the top-performing model at 88% overall accuracy, framed as a self-correcting sequence of weak learners that iteratively focuses on previously misclassified high-income individuals.

**Methods:** Logistic Regression (L1/L2), Ridge, Lasso, Decision Tree, Random Forest, AdaBoost, Gradient Boosting, SVM, KNN
**Dataset:** U.S. Census Adult Income (UCI)
**Key result:** Gradient Boosting achieves 88% accuracy; regularized models show diminishing returns over tree-based alternatives

---

### Text Clustering and Topic Modeling
**File:** [Text Clustering.ipynb](https://github.com/bckenz-ai/machine-learning-projects/blob/main/Text%20Clustering.ipynb)

Applies unsupervised NLP to 2,000 unlabelled IMDB movie reviews to discover latent thematic and emotional structures without ground-truth labels. Contrasts K-Means clustering with Latent Dirichlet Allocation (LDA). K-Means with K=2 successfully aligns with binary sentiment polarity (positive/negative), while LDA proves better suited for uncovering underlying narrative topics such as acting quality, genre conventions, and storytelling style.

**Methods:** K-Means Clustering, Latent Dirichlet Allocation (LDA), TF-IDF, Bag-of-Words
**Dataset:** IMDB Movie Reviews (2,000 unlabelled)
**Key result:** K-Means recovers sentiment polarity; LDA uncovers interpretable thematic topics

---

## Stack

`Python` `Scikit-learn` `NLTK` `spaCy` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Jupyter Notebook`

---

## Context

These notebooks were produced as assessed coursework for B.S. Data Science and Analytics at the University of Santo Tomas, Manila (2024–2028). Each represents an independent analytical report with a defined problem statement, methodology, and written interpretation of results.
