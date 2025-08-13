# Anonymizer
A compilation of natural language processing models that anonymize documents by identifying and replacing sensitive information. The anonymizer preserves critical context that allows for secondary linguistic analyses on anonymized text.

# SoTA supported models

| Model | Dataset | Costumization | Documentation |
|  ---  | ------- | ------------- | ------------- |
| [DistilBERT](https://huggingface.co/elastic/distilbert-base-uncased-finetuned-conll03-english) | [Conll-03](https://paperswithcode.com/dataset/conll-2003)   |  [Fine-tune / Train](https://huggingface.co/docs/transformers/training) | [Huggingface](https://github.com/huggingface/transformers) |
| [RoBERTa](https://huggingface.co/philschmid/distilroberta-base-ner-conll2003) | [Conll-03](https://paperswithcode.com/dataset/conll-2003)   |  [Fine-tune / Train](https://huggingface.co/docs/transformers/training) | [Huggingface](https://github.com/huggingface/transformers) |
| [BERT](https://huggingface.co/dslim/bert-base-NER) | [Conll-03](https://paperswithcode.com/dataset/conll-2003)   |  [Fine-tune / Train](https://huggingface.co/docs/transformers/training) | [Huggingface](https://github.com/huggingface/transformers) | 
| [FLERT](https://huggingface.co/flair/ner-english-large) | [Conll-03](https://paperswithcode.com/dataset/conll-2003)   |  [Fine-tune / Train](https://github.com/flairNLP/flair/blob/master/resources/docs/TUTORIAL_7_TRAINING_A_MODEL.md) | [fairNLP](https://github.com/flairNLP/flair) |
| [FLAIR](https://huggingface.co/flair/ner-english) | [Conll-03](https://paperswithcode.com/dataset/conll-2003)   |  [Fine-tune / Train](https://github.com/flairNLP/flair/blob/master/resources/docs/TUTORIAL_7_TRAINING_A_MODEL.md) | [fairNLP](https://github.com/flairNLP/flair) |
| [Stanford](https://nlp.stanford.edu/software/CRF-NER.html) | [MUC](https://www-nlpir.nist.gov/related_projects/muc/muc_data/muc_data_index.html)   |  [Fine-tune / Train](https://nlp.stanford.edu/software/crf-faq.html#a) | [Stanford](https://github.com/stanfordnlp/stanza) |
| [Spacy](https://spacy.io/universe/project/video-spacys-ner-model) | [OntoNotes](https://catalog.ldc.upenn.edu/LDC2013T19)   |  [Fine-tune / Train](https://spacy.io/usage/training) | [Spacy](https://github.com/explosion/spaCy)
| [NLTK](https://www.nltk.org/api/nltk.corpus.html) | [NLTK corupus](https://www.nltk.org/api/nltk.corpus.html)   |  [Fine-tune / Train](https://www.nltk.org/book/ch07.html) | [NLTK](https://www.nltk.org/) |
| [Presidio](https://microsoft.github.io/presidio/) | [Conll-03](https://paperswithcode.com/dataset/conll-2003)   |  [Fine-tune / Train](https://microsoft.github.io/presidio/tutorial/11_custom_anonymization/) | [Presidio](https://github.com/microsoft/presidio) |

# Quickstart

## Requirments and installation
The project is based on Python 3.9.12. If python is not installed, use [Anaconda distribution](https://docs.anaconda.com/anaconda/install/windows/) to install it. 

``` sh
# Create conda env (optional)
conda create --name anonymizer python=3.9
conda activate anonymizer

# Install package+dependencies
pip install -r requirements.txt

# Download spaCy models
python -m spacy download en_core_web_lg
python -m spacy download en_core_web_trf

```

## Run tests

The [examples](/examples) folder contains a sample input file that can be processed using the [anonymizer_tool.ipynb](./anonymizer_tool.ipynb)

## [License](/LICENSE)

Copyright (c) 2022 dcl91

The MIT License (MIT)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
