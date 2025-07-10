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

### Data collection
Extracted works from Domínio Público, Wikisource, and other open literary repositories from Machado de Assis, Lima Barreto and Graciliano Ramos. 

### Preprocessing
Cleaned and segmented texts into chunks. Removed metadata, normalized punctuation and spacing.

### Stylometry analysis
Sentence length distributions; type/token ratio for lexical richness; POS and dependency pattern frequencies; use of passive voice, punctuation, and conjunctions.

### Modeling
- Baseline: TF-IDF + logistic regression;
- Advanced: fine-tuned BERTimbau for multiclass classification.

### Style transfer
- Fine-tuning GPT-2 using selected author corpus;
- Prompt-based paraphrasing into literary style;
- Evaluation (manual + stylometric).

## Results (WIP)
Baseline model achieves ~70% accuracy in classification.
Transformer-based model shows improved performance and author-specific confusion patterns.
Stylometric profiles reveal stricking differences in sentence structure and lexical richness.

_(Full metrics and visualizations coming soon)_
