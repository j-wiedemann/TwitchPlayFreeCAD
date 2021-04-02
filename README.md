# TwitchPlayFreeCAD
https://www.twitch.tv/freecadfrance

Le concept est de modéliser des objets à l'aide de commandes depuis le tchat. Il y a des objectifs à atteindre, vousp ouvez les connaitre en tapant la commande **!objectif**. Pour savoir si l'objectif est atteint et passer au suivant, taper la commande **!check**.
Pour l'instant seul quelques primitives et quelque opérations booléennes sont disponible. Mais on peut déjà faire bveaucoup avec.
Voici la liste des commandes disponibles et de leur fonction.

**/!\ Lorsque vous faites référence à un objet éxistant la casse est prise en compte, il faut donc écrire avec les majuscules.**

## CRÉATION

### Créer un pavé

Vous pouvez créer un cube avec la commande !cube. Si aucun parametre n'est précisés le cube fera 10 mm de coté.

!cube longueur largeur hauteur

longueur = valeur numérique

largeur = valeur numérique

hauteur = valeur numérique

ex: !cube 10 20.5 2

alias: box, parallelepipede, pave


### Créer un cylindre

Vous pouvez créer un cylindre avec la commande !cylindre. Si aucun paramètre n'est précisés le cylindre aura un rayon de 2 mm et une hauteur de 10 mm.

!cylindre rayon hauteur 

rayon = valeur numérique

hauteur = valeur numérique

ex: !cylindre 5.5 20

alias: cylindre, cylinder, cyl


### Créer une sphère

Vous pouvez créer une sphère avec la commande !sphere. Si aucun paramètre n'est précisés la sphere aura un rayon de 5 mm.

!sphere rayon

rayon = valeur numérique

ex: !sphere 10

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


OPÉRATIONS BOOLÉENNE

!soustraction base outils 

ex: !soustraction Cube Cylindre

!fusion objet1 objet2

ex: !fusion Cube Cylindre

!intersection objet1 objet2

ex: !intersection Cybe Cylindre

MODIFICATIONS

!parametre objet propriété valeur

ex: !parametre Cube Length 12



!supprimer objet

ex: !supprimer Cube



INFORMATION

!information objet

ex: !information Cube



!annotation état

!annotation visible/invisible



VISUELLE

!color



!transparence Objet Valeur



CAMERA

!vue direction 

ex: !vue gauche

paramètres disponibles:

iso, dim, tri, dessus, 

dessous, gauche, droite, 

devant, derriere, +, -, tout


