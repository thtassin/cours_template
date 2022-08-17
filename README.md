# cours_template

 > Modèle général pour le polycopié d'un cours (chapitres, travaux dirigés, fiches méthodes, ...)

## Présentation
Ce projet comporte trois paquets 

1. `cours.sty` : fournit un modèle général pour le cours en lui-même et les travaux dirigés. 
2. `methode.sty` : fournit un modèle général pour des fiches méthodes
3. `theme.sty` : permet de modifier les couleurs de différents objets.

## Modèle général pour la partie cours et la partie exercice
`cours.sty` constitue le fichier principal de ce projet. Pour l'utiliser, il suffit d'ajouter `\usepackage{cours}` dans le prémbule général. Ce paquet possède une option `student` dont l'utilité sera décrite plus tard. Il permet de définir différents environnements qui reposent pour la plupart sur l'itilisation de `tcolorbox` (https://www.ctan.org/pkg/tcolorbox). Les couleurs des différents objets peut-être modifiée via le fichier `theme.sty`. La couleur des sections est notamment définie par la commande `\sectioncolor`.

### Environnements
#### Objectifs
  ```latex
  \begin{objectif}
    \item Objectif 1
    \item Objectif 2
  \end{objectif}
  ```
  La couleur du cadre peut-être modifiée via la commande `\objectifcolor` définie dans `theme.sty`. 
#### Définition
  ```latex
  \begin{defn}{Titre}
    Contenu
  \end{defn}
  ```
  La couleur en arrière-plan du cadre peut-être modifiée via la commande `\defncolor` définie dans `theme.sty`. 
#### Remarque
```latex
\begin{rema}
    Contenu
 \end{rema}
 ```
#### Attention
  ```latex
  \begin{Attention}
    Contenu
  \end{Attention}
  ```
  La couleur du cadre du titre peut-être modifiée via la commande `\attentioncolor` définie dans `theme.sty`.
#### Exemple,
  ```latex
  \begin{exemple}{Titre}
    Contenu
  \end{exemple}
  ```
#### Travaux dirigés
```latex
 \begin{td}{Titre}
  Contenu
 \end{td}
 ```
 L'appel de l'environnement ajoute une entrée **Exercices** à la table des matières. 
#### Correction
```latex
\begin{corr}{Title}
 Contenu
 \end{corr}
 ```
 L'appel de l'environnement ajoute une entrée **Correction** à la table des matières.

### Section
`cours.sty` fournit deux nouveaux types de section, `exercice` et `correction` définis grâce à la commande `titleclass` de `titlesec' (https://www.ctan.org/pkg/titlesec). Ce niveau de section n'apparaît pas dans la table des matières.

### Option
L'option `student` permet de supprimer les corrections, de faire disparaître le contenu des exemples et de créer un texte à trou lorsqu'elle
est activée. Une commande `\blank{mot}` rend possible cette dernière fonctionnalité.

## Modèle général pour une fiche méthode
`methode.sty` permet de générer rapidement un document indépendant du reste du cours. Pour l'utiliser, il suffit d'ajouter `\usepackage{methode}` dans le préambule général du fichier. Les environnements de `cours.sty` sont disponibles dans cette mise en page. Le fichier fournit une fonction supplémentaire `Entete` qui permet de générer le titre de la fiche méthode.
```latex
\Entete{titre}
```
