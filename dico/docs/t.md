## Time series

Les séries temporelles peuvent encore de nombreux défis aux modèles de deep learning
(dépendances pouvant être très longues, signaux faibles...)
et de nombreux modèles sont imaginés pour tenter de résoudre ces problèmes, comme
les modèles informer,
autoformer,
fedformer,
etsformer,
ssdnet,
N-Hits,
TS2Vec, ...

Voir aussi le papier "Transformer with Sparse Attention Mechanism for Industrial Time Series Forecasting"


## Traitement automatique du langage naturel

Le TAL (Traitement Automatique du Langage Naturel) est un des domaines de recherche
à la pointe du deep learning depuis 2018. Il inclut des applications comme la traduction
automatique, les chatbots, le résumé automatique, la transcription de la parole, etc.
Les plus gros modèles de deep learning sont, et de très loin, ceux en TAL.

Voir aussi [Embeddings](../e/#embeddings)

## Transformer

Le modèle qui a complètement remplacé toute la famille
des réseaux récurrents (RNN, LSTM, GRU...) par une nouvelle
famille basée sur la self-attention.
Pourquoi les transformers sont meilleurs ?
Parce que les empiler permet de capturer l'information provenant
de corpus textuels de plus en plus gigantesques, tout comme les
CNN avec les gros corpus d'images.
Les transformers ont révolutionné le TAL, et sont à la base de
tous les modèles récents du domaine: T0pp, GPT-J, BERT, GPT-1.2.3, RoBERTa,
ALBERT, XL-NET, T5, BART...

## Transformers

Est le nom d'une des librairies python les plus utilisées en 2022 pour
accéder et manipuler de très nombreux modèles d'embeddings.

```
pip install transformers
```

