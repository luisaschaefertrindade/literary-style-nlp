# Literary style analysis of Portuguese-speaking authors and multiclass classification
## Project overview
The present project explores the analysis of literary style of Portuguese-speaking authors, combining computational linguistics, stylometry and natural language processing. The selected authors were active during the second half of the 19th century and/or the first half of the 20th century: Machado de Assis, Lima Barreto, Graciliano Ramos, and Eça de Queiroz. While having authors from other Portuguese-speaking countries would have greatly enriched this project, as well as including the voices of women, it is hard to find prose with these characteristics in the public domain.   

## Objectives
### Author classification
Train models to predict the author of a given excerpt using machine learning and transformer-based NLP.

### Style analysis
Extract and compare stylistic features such as sentence length, lexical richness, punctuation, syntactic patterns.

### Style transfer (experimental)
Develop a paraphrasis tool to generate texts in the style of specific authors, starting with GPT-2 fine-tuned on Machado de Assis.

## Tools
- Python (3.10+)
- scikit-learn, pandas, numpy
- spaCy (pt_core_news_sm)
- matplotlib, seaborn
- Streamlit (for demo)

## Methodology
The project is structured in five main steps: data collection, preprocessing, stylometry analysis, modeling, and multiclass classification.

### 1. Data collection
Extracted works from Domínio Público, Wikisource, and other open literary repositories from Machado de Assis and Graciliano Ramos. 

### 2. Preprocessing
Cleaned and segmented texts into chunks. Removed metadata, normalized punctuation and spacing.

### 3. Stylometry analysis
Sentence length distributions; type/token ratio for lexical richness; POS and dependency pattern frequencies; use of passive voice, punctuation, and conjunctions.

### 4. Modeling
- Baseline: TF-IDF + logistic regression;
- Advanced: fine-tuned BERTimbau for multiclass classification.

### 5. Multiclass classification
- Fine-tuning BERTimbau with the corpus;
- Evaluating its performance in classifying each author.

## Results (WIP)
The following classification report shows the authors' styles are not as distinguishable by the baseline model, achieving ~50% accuracy:

                  precision    recall  f1-score   support

  Eça de Queiroz       0.44      0.35      0.39      1090
Graciliano Ramos       0.61      0.70      0.66      1487
    Lima Barreto       0.46      0.27      0.34      1090
Machado de Assis       0.49      0.62      0.54      1596

        accuracy                           0.52      5263
       macro avg       0.50      0.49      0.48      5263
    weighted avg       0.51      0.52      0.50      5263

The confusion matrix further illustrates this:
<img width="658" height="565" alt="image" src="https://github.com/user-attachments/assets/1fd7e55e-fd95-49a4-ba5c-2a0cf4fc09cb" />

The error rate can indicate an overlap or shared vocabulary, as they are both from the same period and writing was still heavily influenced by Portugal.

### Sentence length
<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/42333276-5b77-4be6-8ee0-4b781f9e3e6b" />

Eça de Queiroz tends to use longer sentences on average, favoring complex sentence structures. Graciliano Ramos tends to be more concise and direct.

### PCA on vocabulary-related stylometric features
<img width="789" height="590" alt="image" src="https://github.com/user-attachments/assets/8a86a93f-90a8-46e4-a61b-c3ca20f8a693" />

### BERTimbau performance
Transformer-based model shows improved performance and author-specific confusion patterns.

_(Full metrics and visualizations coming soon)_

## Author
**Luísa Schaefer Trindade**
Computational Linguist | NLP Researcher
GitHub: [luisaschaefertrindade](https://github.com/luisaschaefertrindade/) | LinkedIn: [luisaschaefertrindade](https://www.linkedin.com/in/luisaschaefertrindade/?locale=en_US)
