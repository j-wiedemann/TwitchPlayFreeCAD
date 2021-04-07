# TwitchPlayFreeCAD
https://www.twitch.tv/freecadfrance

Le concept est de modéliser des objets à l'aide de commandes depuis le tchat. Vous pouvez donc piloter FreeCAD depuis le tchat à l'aide de plusieurs commandes. Il y a des objectifs à atteindre, vous pouvez en prendre connaissance en tapant la commande `!objectif`. Pour savoir si l'objectif est atteint et passer au suivant, taper la commande `!check`.
Pour l'instant seul quelques primitives et quelques opérations booléennes sont disponible. Mais on peut déjà faire beaucoup avec ces simples commandes.

Voici la liste des commandes disponibles et de leur fonction.

**/!\ Lorsque vous faites référence à un objet éxistant la casse est prise en compte, il faut donc écrire avec les majuscules.**

## CRÉATION
Ces commandes permettent de créer des primitives géométrique.

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
> !cube 10 20.5 2


### Créer un cylindre

Vous pouvez créer un cylindre avec la commande `!cylindre`. Si aucun paramètre n'est précisés le cylindre aura un rayon de 2 mm et une hauteur de 10 mm.

#### commande:
`!cylindre rayon hauteur`

#### arguments:
* `rayon` (valeur numérique pour le rayon en mm)
* `hauteur` (valeur numérique pour la hauteur en mm)

#### alias:
cylinder, cyl

#### exemples:
> !cylindre 5.5 20


### Créer une sphère

Vous pouvez créer une sphère avec la commande !sphere. Si aucun paramètre n'est précisés la sphere aura un rayon de 5 mm.

#### commande:
`!sphere rayon`

#### arguments:
* `rayon` (valeur numérique pour le rayon en mm)

#### exemples:
> !sphere 10

## OPÉRATIONS BOOLÉENNE
Ces commandes permettent de faire des opérations logique sur des primitives existantes. 
### Soustraction
Une soustraction booléenne enlève le volume de la forme de l'outils à la forme de base.
#### commande:
`!soustraction base outils`

#### arguments:
* `base` (objet qui sert de base à l'opération booléenne)
* `outils` (objet qui va supprimer du volume à la base)

#### alias:
sub

#### exemples
> !soustraction Cube Cylindre

### Fusion
La fusion permet d'unir le volume de deux objets.

#### commande:
`!fusion Objet1 Objet2`

#### arguments:
* `Objet1` (objet qui va être fusionné)
* `Objet2` (objet qui va être fusionné)

#### alias:
fuse

#### exemples
> !fusion Cube Cylindre

### Intersection
Une intersection permet d'obtenir la forme qui est commune à deux objets.
#### commande:
`!intersection Objet1 Objet2`

#### arguments:
* `Objet1` (objet qui va être mis en commun)
* `Objet2` (objet qui va être mis en commun)

#### alias:
common

#### exemples
> !intersection Cybe Cylindre


## TRANSFORMATIONS
### Translation

Pour déplacer un objet on utilise la commande `!translation`. Le déplacement est relatif à la position actuelle de l'objet.

#### commande:
`!translation Objet x y z`

#### arguments:
* `Objet` (nom de l'objet à déplacer /!\ à la casse)
* `x` (valeur numérique en mm pour la translation selon l'axe X)
* `y` (valeur numérique en mm pour la translation selon l'axe Y)
* `z` (valeur numérique en mm pour la translation selon l'axe Z)

#### alias:
move, translate, deplacer

#### exemple:
> !translation Cube 10 20 30


### Rotation

Pour pivoter un objet on utilise la commande !rotation. Le centre de rotation est défini par son placement.

#### commande:
`!rotation Objet angle axe`

#### arguments:
* `Objet` (nom de l'objet à déplacer /!\ à la casse)
* `angle` (valeur numérique en ° pour l'angle de rotation)
* `axe` (défini l'axe de rotation, peut être `x`, `y` ou `z`)

#### alias:
rot

#### exemple:
> !rotation Cube 45 z

### Paramètre
Cette commande permet de changer un paramètre d'une primitive.

#### commande:
`!parametre Objet Propriété valeur`

#### arguments:
* `Objet` (nom de l'objet à déplacer /!\ à la casse)
* `Propriété` (nom de la propriété /!\ en anglais et sensible à la casse)
* `valeur` (nouvelle valeur de la propriété)

#### alias:
param, parameter

#### exemple:
> !parametre Cube Length 12


### Supprimer
Cette commande permet de supprimer un objet

#### commande:
`!supprimer objet`

#### alias:
destroy, remove, suppr, del

#### exemple:
> !supprimer Cube

### Annuler
Cette commande permet d'annuler la denière commande.
#### commande:
`!ctrlz`

#### alias:
annuler, cancel, undo

### Refaire
Cette commande permet de refaire la dernière opération précédement annuler.

#### commande:
`!ctrly`

#### alias:
retablir, refaire, redo

## INFORMATIONS

`!information objet`

#### exemple:
> !information Cube


## AFFICHAGE

### Transparence

`!transparence Objet Valeur`

### Annotation

`!annotation état`

!annotation visible/invisible

### Couleur
Pas encore implémenter.
`!color`


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
cam, view

#### exemple:
> !vue gauche


## CHALLENGE

Il y a des objectifs à atteindre !

### Objectif
Avec la commande `!objectif` vous pouvez connaitre le plan de l'objectif en cours.

#### alias:
goal

### Vérification
Avec la commande `!valider` vous pouvez vérifier si l'objectif est atteint.

#### alias:
check, verifier, verification
