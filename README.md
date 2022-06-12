# cours_template

 > Modèle général pour le polycopié d'un cours (chapitres, travaux dirigés, fiches méthodes, ...)

## Présentation
Ce projet comporte trois paquets 

1. `cours.sty` : fournit un modèle général pour le cours en lui-même et les travaux dirigés. 
2. `methode.sty` : fournit un modèle général pour des fiches méthodes
3. `theme.sty` : permet de modifier les couleurs de différents objets.

## Usage
`cours.sty` constitue le fichier principal de ce projet. Il permet de définir différents environnements

- Définition,
  ```latex
  \begin{defn}{Titre}
    Contenu
  \end{defn}
  ```
- Remarque,
  \begin{rema}
    Contenu
  \end{rema}
- Attention,
  \begin{Attention}
    Contenu
  \end{Attention}
- Exemple,
  \begin{exemple}{Titre}
    Contenu
  \end{exemple}
- Travaux dirigés,
- Correction.


## License

