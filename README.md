# Literary style classification and stylization of Brazilian authors
## Project overview
The present project explores the classification of literary style, as well as text generation in the style of great Brazilian authors, combining computational linguistics, stylometry and natural language processing.

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
- HuggingFace Transformers (BERTimbau, GPT-2)
- spaCy (pt_core_news_sm)
- matplotlib, seaborn
- Streamlit (for demo)

## Methodology
The project is structured in five main steps: data collection, preprocessing, stylometry analysis, modeling, and style transfer.

### 1. Data collection
Extracted works from Domínio Público, Wikisource, and other open literary repositories from Machado de Assis and Graciliano Ramos. 

### 2. Preprocessing
Cleaned and segmented texts into chunks. Removed metadata, normalized punctuation and spacing.

### 3. Stylometry analysis
Sentence length distributions; type/token ratio for lexical richness; POS and dependency pattern frequencies; use of passive voice, punctuation, and conjunctions.

### 4. Modeling
- Baseline: TF-IDF + logistic regression;
- Advanced: fine-tuned BERTimbau for multiclass classification.

### 5. Style transfer
- Fine-tuning GPT-2 using selected author corpus;
- Prompt-based paraphrasing into literary style;
- Evaluation (manual + stylometric).

## Results (WIP)
Baseline model achieves ~80% accuracy in classification. The following classification report shows its reasonable performance:

                  precision    recall  f1-score   support

Graciliano Ramos       0.78      0.74      0.76      1487
Machado de Assis       0.77      0.81      0.79      1596

        accuracy                           0.77      3083
       macro avg       0.78      0.77      0.77      3083
    weighted avg       0.78      0.77      0.77      3083

The confusion matrix further illustrates this:
<img width="548" height="455" alt="image" src="https://github.com/user-attachments/assets/a1e4b907-b7e3-47cc-8932-23256d58a806" />

The feature set investigated in this project captures important stylistic differences. However, the ~20% error rate can indicate an overlap or shared vocabulary, as they are both 20th-century Brazilian authors.

### Sentence length
<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/d37cd634-8675-4853-824e-11b1039ef8ea" />

Machado de Assis tends to use longer sentences on average, favoring complex sentence structures. Graciliano Ramos tends to be more concise and direct.

Transformer-based model shows improved performance and author-specific confusion patterns.
Stylometric profiles reveal stricking differences in sentence structure and lexical richness.

_(Full metrics and visualizations coming soon)_

## Author
**Luísa Schaefer Trindade**
Computational Linguist | NLP Researcher
GitHub: luisaschaefertrindade | LinkedIn: 
