## Embeddings

(*Fr: plongements*)

Ce terme fait référence à une représentation vectorielle des observations.
Il est souvent (mais pas seulement) utilisé en TAL pour représenter les mots,
ou les phrases, ou les documents, avec un seul vecteur.
Avant 2018, un mot du lexique était souvent représenté par un unique vecteur,
toujours le même, par exemple calculé avec les modèles Word2Vec ou Glove.
D'autres modèles existaient pour les phrases, comme Skip-thought.
Depuis 2018, le vecteur d'un même mot change en fonction du reste de la phrase,
on parle d'embeddings contextuels, ce qui permet de désambiguiser le sens du
mot "avocat" par exemple.
Les modèles qui calculent ces vecteurs sont par exemple BERT, T5, BART, GPT,
G-Shard, Wu Dao 2.0...

Ces modèles sont entraînés sur d'immenses bases de données extraites du Web et
sont les plus gros modèles de deep learning aujourd'hui.
Les vecteurs qu'ils produisent contiennent des informations sur tous les aspects
linguistiques des mots (morphologie, syntaxe, sémantique, etc.), mais aussi sur
des faits liés au mot (par exemple, tout ce que JFK a réalisé d'important dans sa vie).

Les plus gros modèles sont en anglais; il en existe également dans d'autres langues,
mais les solutions les plus performantes restent aujourd'hui de soit traduire d'abord
en anglais pour pouvoir utiliser les meilleurs modèles, soit utiliser des modèles
multi-lingues comme XLMR, qui fusionnent et partagent l'information entre de nombreuses 
langues.

Ces modèles gigantesques offrent les meilleures performances, mais soulèvent de nombreux
problèmes éthiques (ils peuvent reproduire voire amplifier les biais des données,
ils contiennent des informations privées, ils sont utilisés dans toutes les technologies
en TAL mais seule une poignée d'acteurs mondiaux les contrôle...) et écologiques
(le coût-carbone pour les entraîner est exhorbitant) qui focalisent l'attention des chercheurs depuis 2020.

Voir aussi [LLM](../l/#language-models).

