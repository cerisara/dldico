## MLM

Le Masked Language Modeling (MLM) est un critère d'apprentissage des modèles
d'embeddings qui s'apparente à celui utilisé à l'origine pour les modèles de langage:
ce dernier prédit le mot suivant, tandis que le MLM prédit un mot masqué aléatoire
dans la phrase. Les modèles résultants ne sont donc pas a priori *causaux*, car ils
ne prédisent pas de gauche à droite mais utilisent également les mots du contexte droit.

Voir aussi [Embeddings](../e/#embeddings).

