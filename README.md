# TwitchPlayFreeCAD
https://www.twitch.tv/freecadfrance

Le concept est de modéliser des objets à l'aide de commandes depuis le tchat. Il y a des objectifs à atteindre, vousp ouvez les connaitre en tapant la commande **!objectif**. Pour savoir si l'objectif est atteint et passer au suivant, taper la commande **!check**.
Pour l'instant seul quelques primitives et quelque opérations booléennes sont disponible. Mais on peut déjà faire bveaucoup avec.
Voici la liste des commandes disponibles et de leur fonction.

**/!\ Lorsque vous faites référence à un objet éxistant la casse est prise en compte, il faut donc écrire avec les majuscules.**

## CRÉATION

### Créer un cube

Vous pouvez créer un cube avec la commande `!cube`. Si aucun parametre n'est précisé le cube fera 10 mm de coté.

#### commande:
`!cube longueur largeur hauteur`

#### arguments:
* `longueur` (valeur numérique pour la longueur en mm)
* `largeur` (valeur numérique pour la largeur en mm)
* `hauteur` (valeur numérique pour la hauteur en mm)

#### alias:
box, parallelepipede, pave

#### exemples:
> ex: !cube 10 20.5 2


### Créer un cylindre

Vous pouvez créer un cylindre avec la commande !cylindre. Si aucun paramètre n'est précisés le cylindre aura un rayon de 2 mm et une hauteur de 10 mm.

#### commande:
`!cylindre rayon hauteur`

#### arguments:
* `rayon` (valeur numérique pour le rayon en mm)
* `hauteur` (valeur numérique pour la hauteur en mm)

#### alias:
cylinder, cyl

#### exemples:
ex: !cylindre 5.5 20


### Créer une sphère

Vous pouvez créer une sphère avec la commande !sphere. Si aucun paramètre n'est précisés la sphere aura un rayon de 5 mm.

!sphere rayon

rayon = valeur numérique

ex: !sphere 10

## OPÉRATIONS BOOLÉENNE
### Soustraction
!soustraction base outils 

ex: !soustraction Cube Cylindre

### Fusion
!fusion objet1 objet2

ex: !fusion Cube Cylindre

### Intersection
!intersection objet1 objet2

ex: !intersection Cybe Cylindre



## TRANSFORMATIONS
### Translation

Pour déplacer un objet on utilise la commande !translation. Le déplacement est relatif à la position actuelle de l'objet.

!translation Objet x y z 

ex: !translation Cube 10 20 30

alias: deplacer, translate, move


### Rotation

Pour pivoter un objet on utilise la commande !rotation. Le centre de rotation est défini par son placement.

!rotation Objet angle axe 

ex: !rotation Cube 45 z

axes disponibles:

x ou y ou z

### Paramètre
!parametre objet propriété valeur

ex: !parametre Cube Length 12

### Supprimer

!supprimer objet

ex: !supprimer Cube


## INFORMATIONS

!information objet

ex: !information Cube


## AFFICHAGE

### Transparence

!transparence Objet Valeur

### Annotation

!annotation état

!annotation visible/invisible

### Couleur
Pas encore implémenter.
!color


## CAMERA

#### commande:
`!vue direction` 

#### arguments:
* `iso` (vue isométrique)
* `dim` (vue dimétrique
* `tri` (vue trimétrique)
* `dessus` (vue de dessus)
* `dessous` (vue de dessous)
* `gauche` (vue de gauche)
* `droite` (vue de droite)
* `devant` (vue de devant)
* `derriere` (vue de derriere)
* `+` (zoom arrière)
* `-` (zoom avant)
* `tout` (tout voir)

#### alias:
cam

#### exemple:
ex: !vue gauche


## CHALLENGE

Il y a des objectifs à atteindre !

### Objectif
Avec la commande `!objectif` vous pouvez connaitre le plan de l'objectif en cours.

### Vérification
Avec la commande `!verification` vous pouvez vérifier si l'objectif est atteint.

