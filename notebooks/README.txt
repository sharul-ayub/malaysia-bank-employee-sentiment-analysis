Split notebook workflow

01_data_preparation_and_sentence_splitting.ipynb
    raw review data -> sentence-level rows -> manual inspection export

02_ai_sentiment_labeling_and_manual_check.ipynb
    sentence rows -> zero-shot labels -> manual checking -> binary labelled data

03_text_cleaning_and_normalization.ipynb
    labelled sentences -> cleaning + slang/abbreviation/typo normalisation

04_tokenization_stopwords_and_lemmatization.ipynb
    cleaned sentences -> spaCy tokens -> stopwords -> lemmas -> model-ready text

05_model_training_and_tuning.ipynb
    train/test split -> BOW/TF-IDF baseline -> vectorizer tuning -> model tuning

06_evaluation_error_analysis_and_model_export.ipynb
    final candidate comparison -> metrics -> confusion matrix -> errors -> final model

Important source-code fixes included:
- Project year filter set to 2024-2026 (source narrative) instead of pasted 2012-2023 code.
- Manual checked sentence file is used for labelling when available.
- Contractions are expanded before apostrophe/punctuation cleanup.
- Lemmatization correctly joins token lists before passing them to spaCy.
- Missing TF-IDF tuning block was added because later pasted code referenced it.
- Relative repository paths replace personal Google Drive paths.

Additional output folders used:
- data/processed/07_model_ready.csv
- models/
