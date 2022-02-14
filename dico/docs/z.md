## Zero-shot learning

En TAL, l'une des marottes du début 2021 consiste à exploiter les gros transformers appris
sur tout l'anglais (T5, BART...) pour résoudre des tâches de NLP sans apprentissage, simplement
en ajoutant la description *D* de la tâche en anglais aux observations *X*, le modèle étant
capable d'inférer le lien sémantique entre *D,X* et la solution *Y*.

Refs:
[adapters](https://arxiv.org/pdf/2101.00420.pdf)
[entailment](https://arxiv.org/pdf/2010.02584.pdf)

