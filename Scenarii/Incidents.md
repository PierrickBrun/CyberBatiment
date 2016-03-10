Incidents
=========
Régler Piggybacking
------------

**Contexte** [Bruno] est gardien, [Bernardo] et [Marie] sont deux spectateurs qui sont entrés à deux
dans le même [Bisas] n°12 après avoir utilisé le billet de Marie. Le [Bisas] n°12 fait partie du
[PointAcces] n°5 menant à la Zone “Tribunes”, les tribunes du stade de Nilton Santos. Le piggybacking à été détecté.

**Intention** Prévenir un gardien pour résoudre l'incident piggybacking

 - 15h30 : Un Piggybacking est détecté par le Système sur le [Bisas] n°12 de la [Zone] "Tribunes"
 - 15h30 : La LED du [Bisas] passe au rouge
 - 15h30 : Un incident est envoyé sur le smartphone du [Gardien] en charge de la [Zone] de l'incident
 - 15h30 : Le [Gardien] en charge de la [Zone] “Tribunes” [Bruno] reçoit sur son smartphone l’[Incident] avec
le numéro du [Bisas] posant problème sous forme d'alerte.
 - 15h32 : [Bruno] ouvre l'alerte
 - 15h34 : [Bruno] se rend sur les lieux de l'incident
 - 15h35 : [Bruno] choisi l’option “Ouvrir portes”
 - 15h35 : Le [Système] commande l’ouverture de la porte du [Bisas] sur la face par laquelle [Marie] et
[Bernardo] sont entrés
 - 15h36 : [Bruno] choisi l’option “Résoudre”
 - 15h36 : L’incident est enregistré comme résolu
 - 15h36 : La LED du [Bisas] s'éteint

Ignorer Incident
--------------------

**Contexte** [Bruno] est gardien de la Zone “Tribunes” limitée à 500 personnes, les tribunes du stade de Nilton Santos sont pleines à 499/500 personnes.

**Intention** Cas d'une zone pleine générant un Incident qui se vide avant que le Gardien n'arrive sur les lieux.

 - 12h00 : Un nouveau spectateur entre dans la [Zone] "Tribunes"
 - 12h00 : Le système génère un incident qui est envoyé sur la smartphone de [Bruno] le prévenant que la [Zone] "Tribunes" est pleine
 - 12h05 : Plusieurs spectateurs sortent de la [Zone] "Tribunes"
 - 12h06 : [Bruno] appuie sur l'option "Traiter" de son smartphone
 - 12h07 : [Bruno] se rend dans la zone de l'incident
 - 12h10 : [Bruno] constate la sortie de plusieurs spectateurs de la [Zone] "Tribunes"
 - 12h10 : [Bruno] appuie sur l'option "Ignorer" sur son smartphone
 - 12h10 : Le Système enregistre l'incident comme ignoré.
