## Deep learning

Réduire le deep learning à la seule application des réseaux de neurones
inventés dans les années 80 à de grandes bases de données sur des GPU puissants,
est équivalent à dire que les langages de programmation actuels (python, go, caml...)
ne sont que l'application d'instructions en langage machine dans de grandes
mémoires RAM, ou que "A la recherche du temps perdu" n'est qu'une suite de lettres sur
de nombreuses pages.

Le deep learning est une évolution majeure du domaine du machine learning, basée sur trois
notions fondamentales qui existaient depuis longtemps, mais dont la combinaison et surtout
l'usage novateur a posé les bases du deep learning: (i) la dérivation automatique, qui permet
d'optimiser de très nombreuses familles de fonctions sans avoir besoin de calculer leur gradient;
(ii) l'apprentissage de bout-en-bout (*end-to-end*), qui permet de combiner toutes les fonctions et sous-modules
que l'on souhaite sans avoir à les optimiser les uns après les autres;
et (iii) l'algorithme de descente de gradient stochastique (*SGD*), qui s'est révélé d'une efficacité
redoutable pour optimiser de telles architectures.

Alors que la recherche en machine learning se focalisait sur l'extraction de features les plus
pertinentes possibles pour quelques modèles prédéfinis équipés d'algorithmes d'optimisation spécifiques,
le deep learning a intégré le calcul de ces features au sein du modèle et s'est focalisé sur
la conception du modèle en entier, optimisé grace au seul algorithme SGD.

A ceci s'ajoute un contexte favorable: de grandes masses de données, et des GPUs à foison, qui rendent
réalisables l'apprentissage de modèles de plus en plus gros qui acquièrent des informations de plus en plus précises.
Ce changement d'échelle a levé un voile sur un nouveau champ d'investigation théorique en machine learning,
inaccessible jusque là: la convexité, jusque là considérée comme importante, ne l'est plus du tout.
les optima locaux, jusque là à proscrire, s'avèrent finalement des alliés précieux; les "saddle points" devenant
les nouveaux ennemis; l'overfitting, jusque là à éviter à tout prix, devient un passage obligé vers le
succès (voir la [double descente](../d/#double-descente)).
Et surtout, comment expliquer les étonnantes capacités de généralisation ainsi obtenues ?
Quelles propriétés géométriques possède vraiment l'espace en très grande dimension des paramètres ?
Ce nouvel eldorado théorique est exploré actuellement par de nombreux chercheurs,
mais reste bien mystérieux.

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

