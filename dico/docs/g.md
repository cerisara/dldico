## GAN

Generative Adversarial Network: plutôt que générer des données
en minimisant simplement la distance entre les données générées
et les exemples réels (c'est l'apprentissage classique), un bien
meilleur générateur peut être obtenu en lui apprenant à générer
des exemples qui trompent un autre réseau, qui est lui entraîné
à discriminer les exemples réels des faux.
Pas facile à faire converger, mais d'innombrables progrès ont
été réalisés (cf. par ex. Wasserstein-GAN).

