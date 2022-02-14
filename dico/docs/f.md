## Federated learning

Comment continuer à entraîner des modèles sans divulguer les données privées ?
Comment se passer des fermes de GPU au coût écologique important ?
Une solution à ces deux problèmes (et à d'autres) pourrait bien être le
federated learning (FL), qui apprend les modèles localement et les fusionne ensuite
soit globalement, soit de manière décentralisée.
D'innombrables variantes de ce principe existent, les plus connues étant connues
sous le nom de "collaborative learning" et "fusion learning".
Il existe de nombreuses formes de FL: cross-silo lorsque les noeuds de calcul locaux
sont puissants, cross-device lorsque l'essentiel du calcul est déporté, horizontal
lorsque les données sont distribuées indépendamment entre les noeuds, vertical lorsque
les noeuds collaborent sur des données en partie partagées, etc.

