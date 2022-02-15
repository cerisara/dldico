## GAN

Generative Adversarial Network: plutôt que générer des données
en minimisant simplement la distance entre les données générées
et les exemples réels (c'est l'apprentissage classique), un bien
meilleur générateur peut être obtenu en lui apprenant à générer
des exemples qui trompent un autre réseau, qui est lui entraîné
à discriminer les exemples réels des faux.
Pas facile à faire converger, mais d'innombrables progrès ont
été réalisés (cf. par ex. Wasserstein-GAN).

## GPT

Famille de modèles de langage, connus pour leur grande taille.
Ils sont basés sur les transformer, mais n'utilisent que la
partie décodeur. Ce sont de purs modèles de langage.
GPT2 est disponible gratuitement, est de taille "raisonnable"
et peut donc être utilisé sur un ordinateur personnel.
GPT3 est beaucoup plus gros et n'est accessible que via une API payante.
Des versions intermédiaires, comme Distill-GPT tentent de concilier
performances et taille gérable.
Le récent GPT-J est gratuit et donnerait
des performances compétitives pour une taille encore gérable sur
des systèmes personnels assez puissants.
Notons que l'utilisation de tels modèles requiert de nombreuses
optimisations, par exemple celles de la famille d'algorithmes Zero-2 et DeepSpeed,
voire parfois de la parallélisation sur plusieurs GPUs,
toutes fonctions accessibles à moindre effort via des librairies comme
**accelerate** ou **pytorch lightning**.

