# Módulo: Introdução ao NLP (Processamento de Linguagem Natural)

Notebooks que fiz durante o módulo de **NLP** do *The AI Engineer Course* (365 Data Science / Udemy).
Cada notebook acompanha uma aula ou um exercício prático e usa Python com NLTK, spaCy, scikit-learn, Gensim e Hugging Face Transformers.

## Conteúdo

| # | Notebook | Tema | Dataset |
|---|----------|------|---------|
| 01 | [Pré-processamento de texto](notebooks/01_text_preprocessing.ipynb) | Lowercase, stopwords, regex, tokenização, stemming, lematização, n-grams | — |
| 02 | [Prática: reviews de hotéis](notebooks/02_practical_preprocessing_hotel_reviews.ipynb) | Pipeline completo de pré-processamento | `tripadvisor_hotel_reviews.csv` |
| 03 | [POS tagging](notebooks/03_pos_tagging.ipynb) | Classificação gramatical com spaCy | — |
| 04 | [Named Entity Recognition](notebooks/04_named_entity_recognition.ipynb) | Reconhecimento de entidades nomeadas | — |
| 05 | [Prática: notícias da BBC](notebooks/05_practical_pos_ner_bbc_news.ipynb) | POS tagging + NER em manchetes | `bbc_news.csv` |
| 06 | [Sentimento baseado em regras](notebooks/06_rule_based_sentiment.ipynb) | TextBlob e VADER | — |
| 07 | [Transformers pré-treinados](notebooks/07_pretrained_transformers.ipynb) | Pipelines de sentimento do Hugging Face | — |
| 08 | [Prática: reviews de livros](notebooks/08_practical_sentiment_book_reviews.ipynb) | VADER vs. Transformer | `book_reviews_sample.csv` |
| 09 | [Bag of Words](notebooks/09_bag_of_words.ipynb) | Vetorização por contagem | — |
| 10 | [TF-IDF](notebooks/10_tf_idf.ipynb) | Vetorização TF-IDF | — |
| 11 | [Topic modelling: LDA](notebooks/11_topic_modelling_lda.ipynb) | Latent Dirichlet Allocation com Gensim | `news_articles.csv` |
| 12 | [Topic modelling: LSA](notebooks/12_topic_modelling_lsa.ipynb) | Latent Semantic Analysis | `news_articles.csv` |
| 13 | [Classificador customizado](notebooks/13_custom_classifier.ipynb) | Regressão Logística e Naive Bayes | — |
| 14 | [**Projeto final: detecção de fake news**](notebooks/14_final_project_fake_news.ipynb) | POS, NER, sentimento, LDA, LSA e classificação de notícias falsas vs. factuais | `fake_news_data.csv` |

## Estrutura

```
nlp/
├── notebooks/         # notebooks numerados na ordem do curso
├── data/              # datasets CSV usados nos exercícios
└── requirements.txt   # versões dos pacotes
```

## Como rodar

O ambiente usa Python 3.11 com conda:

```bash
conda create --name nlp_course_env python=3.11
conda activate nlp_course_env
pip install -r requirements.txt
python -m spacy download en_core_web_sm
python -m ipykernel install --user --name=nlp_course_env
```

Depois abra o Jupyter **a partir da pasta `notebooks/`**, porque os notebooks leem os dados de `../data/`, e escolha o kernel `nlp_course_env`.

## Créditos

Os notebooks e datasets acompanham o curso [Introduction to NLP](https://learn.365datascience.com/courses/nlp), que faz parte do *The AI Engineer Course* da 365 Data Science.
