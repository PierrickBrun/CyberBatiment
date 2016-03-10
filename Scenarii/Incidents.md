Incidents
=========
Régler Piggybacking
------------

**Contexte** [Bruno] est gardien, [Bernardo] et [Marie] sont deux spectateurs qui sont entrés à deux
dans le même [Bisas] n°12 après avoir utilisé le billet de Marie. Le [Bisas] n°12 fait partie du
[PointAcces] n°5 menant à la Zone “Tribunes”, les tribunes du stade de Nilton Santos. Le piggybacking à été détecté.

**Intention** Prévenir un gardien pour résoudre l'incident piggybacking

- Un Piggybacking est détecté par le Système sur le [Bisas] n°12 de la [Zone] "Tribunes"
- La LED du [Bisas] passe au rouge
- Un incident est envoyé sur le smartphone du [Gardien] en charge de la [Zone] de l'incident
- Le [Gardien] en charge de la [Zone] “Tribunes” [Bruno] reçoit sur son smartphone l’[Incident] avec
le numéro du [Bisas] posant problème sous forme d'alerte.
- [Bruno] ouvre l'alerte
- [Bruno] se rend sur les lieux de l'incident
- [Bruno] choisi l’option “Ouvrir portes”
- Le [Système] commande l’ouverture de la porte du [Bisas] sur la face par laquelle [Marie] et
[Bernardo] sont entrés
- [Bruno] choisi l’option “Résoudre”
- L’incident est enregistré comme résolu

Ignorer Incident
--------------------

**Contexte** [Bruno] est gardien de la Zone “Tribunes” limitée à 500 personnes, les tribunes du stade de Nilton Santos sont pleines à 499/500 personnes.

**Intention** Cas d'une zone pleine générant un Incident qui se vide avant que le Gardien n'arrive sur les lieux.

- Un nouveau spectateur entre dans la [Zone] "Tribunes"
- Le système génère un incident qui est envoyé sur la smartphone de [Bruno] le prévenant que la [Zone] "Tribunes" est pleine
- Plusieurs spectateurs sortent de la [Zone] "Tribunes"
- [Bruno] appuie sur l'option "Traiter" de son smartphone
- [Bruno] se rend dans la zone de l'incident
- [Bruno] constate la sortie de plusieurs spectateurs de la [Zone] "Tribunes"
- [Bruno] appuie sur l'option "Ignorer" sur son smartphone
- Le Système enregistre l'incident comme ignoré.
