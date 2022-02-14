## Deep learning

Réduire le deep learning à la seule application des réseaux de neurones
inventés dans les années 80 à de grandes bases de données sur des GPU puissants,
est équivalent à dire que les langages de programmation actuels (python, go, caml...)
ne sont que l'application d'instructions en langage machine dans de grandes
mémoires RAM, ou que "A la recherche du temps perdu" n'est qu'une suite de lettres sur
de nombreuses pages.

Voir aussi [Programmation différentiable](../p/#programmation-differentiable)

## Differential privacy

Le principe de base est d'ajouter du bruit pendant l'apprentissage des modèles, ce qui
permet de réduire théoriquement la probabilité que le modèle divulgue des données
apprises par coeur, prévenant ainsi des attaques sur les modèles de deep learning comme
la "membership inference attack".
Mais le bruit réduit aussi la précision du modèle pour la tâche qu'il est censé réaliser,
et cette réduction des performances se révèle souvent trop importante pour être utilisable
en pratique.

## Distillation

Les gros modèles (teacher) peuvent être "réduits" en transmettant les informations qu'ils ont apprises
à d'autres modèles plus petits (students) mais dont les performances sont quasi-identiques.
Début 2021, on parle aussi de distillation de données, c'est-à-dire de la possibilité de
construire de toutes petites bases de données artificielles qui reproduisent les gradients des
gros modèles. Cette approche permet d'entraîner ensuite un modèle sur très peu de données et
très rapidement. A mon avis, cette piste est intéressante, mais d'autres papiers démontrent que
pour bien généraliser, les modèles *doivent apprendre par coeur* la longue queue de la loi de Zipf,
et je ne suis pas certain que la distillation de datasets le permette (?)

