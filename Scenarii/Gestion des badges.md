Gestion des badges
==========================================
Définir une autorisation
------------------------

**Intention** L’[Administrateur] Michel en charge du groupe “Compétis Hockey mardi 22/03” souhaite ajouter une autorisation d’accès à la zone “Tribune 12B” et “Hall entree tribune 12B” pour le groupe susmentionné. Ceci afin d’autoriser l’accès aux tribunes aux personnes ayant acheté leur billet pour le match du 22 mars de 20h à 23h.

**Contexte** La zone “Tribune 12B” a été créée précédement par le superviseur.


- 18h30 : Michel accède à la fenètre d’ajout d’autorisation sur son poste administrateur
- 18h30 : Il séléctionne le groupe de badge “Compétis Hockey mardi 22/03” parmis les deux groupes dont il est en charge
- 18h31 : Il sélectionne la zone “Tribune 12B” et “Hall entree tribune 12B”
- 18h32 : Il ne sélectionne pas de mois ni de jour de [périodicité] mais spécifie la date: du 22/03/2017 au 22/03/2017
- 18h32 : Il entre l’horaire: De 20h00 à 23h00
- 18h33 : Il clique sur le bouton de validation

L’[autorisation accès] est effective pour les badgeurs du groupe “Compétis Hockey mardi 22/03” le 22/03 à partir de 20h jusqu’à 23h.


Passage non autorisé
--------------------

**Contexte** Virginie est visiteuse, elle vient voir l'épreuve de ski nordique le 17/08/16 au stade de
Nilton-Santos à Rio. Elle se trompe de Billet et essaie de réutiliser celui de la veille lui permettant de
voir le triple saut.

**Intention** Utilisation d'un badge en dehors des horaires d'autorisation et prévention du passage du [Badgeur]

 - 10h57 : Virginie passe son billet 879277246472 possédant un QR code sur la [Badgeuse] 128
 - 10h57 : Le système détermine que le billet n'est pas valide
 - 10h57m25s : La LED de la [Badgeuse] 128 passe au rouge
 - 10h57m30s : La LED du [Bisas] s'éteint



Passage avec piggybacking
-------------------------

**Contexte** Virginie est visiteuse, elle vient voir l'épreuve de triple saut le 16/08/16 au stade de
Nilton-Santos à Rio. Anne essaie de passer dans le [Bisas] avec Virginie pour économiser un Billet.

**Intention** Passage en piggybacking, génération d'un incident et blocage des utilisateurs en attendant la résolution de l'incident.

 - 08h12 : Virginie passe son billet 879277246472 possédant un QR code sur la [Badgeuse] 256
 - 08h12 : La LED de la [Badgeuse] 256 passe au vert
 - 08h12 : La porte du côté de Virginie du [Bisas] correspondant s'ouvre
 - 08h13 : Virginie entre dans le [Bisas]
 - 08h13 : Anne entre dans le [Bisas]
 - 08h13 : La porte ouverte du [Bisas] se ferme
 - 08h13 : La LED du [Bisas] passe au orange
 - 08h13 : Le Système détecte qu’il y a deux personnes à l’intérieur
 - 08h13 : La LED du [Bisas] passe au rouge
 - 08h13 : Le Système déclenche un [Incident]
