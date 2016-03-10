Gestion des badges
==========================================
Définir une autorisation
------------------------

**Intention** [CyberCompetition] est en mesure de communiquer avec l’ERP interne [CyberBatiment] Pour la vente de billets pour le Stade de Nilton Santos

**Contexte** Il existe un [Groupe] “Hockey16012015” dédié à la compétition ayant lieu le 16/01/2017 de 12h à 17h donnant accès au stade dans les horaires de la compétition

21h23 - Un billet pour le Stade de Nilton Santos à été vendu pour la compétition qui aura lieu le 16/01/2017
de 12h à 17h sur la plateforme [CyberCompetition]
21h23 - Le système externe [CyberCompetition] envoie une requète à l’[APIBillets] respectant le format normalisé par l’ERP [CyberCompetition] et contenant les - informations suivantes: Nom du groupe
“Hockey16012015”, Nom du spectateur “Virginie Maris”, Code correspondant au QRCode généré.
21h24 - Le Système recoit et interprète l’information reçue
21h24 - Le Système enregistre numéro du billet dans le [Groupe] “Hockey16012015”
21h24 - Le Système accuse de la création de l'autorisation


Passage non autorisé
--------------------

**Contexte** Virginie est visiteuse, elle vient voir l'épreuve de ski nordique le 17/08/16 au stade de
Nilton-Santos à Rio. Elle se trompe de Billet et essaie de réutiliser celui de la veille lui permettant de
voir le triple saut.

**Intention** Utilisation d'un badge en dehors des horaires d'autorisation et prévention du passage du [Badgeur]

10h57 - Virginie passe son billet 879277246472 possédant un QR code sur la [Badgeuse] 128
10h57 - Le système détermine que le billet n'est pas valide
10h57m25s- La LED de la [Badgeuse] 128 passe au rouge
10h57m30s- La LED du [Bisas] s'éteint



Passage avec piggybacking
-------------------------

**Contexte** Virginie est visiteuse, elle vient voir l'épreuve de triple saut le 16/08/16 au stade de
Nilton-Santos à Rio. Anne essaie de passer dans le [Bisas] avec Virginie pour économiser un Billet.

**Intention** Passage en piggybacking, génération d'un incident et blocage des utilisateurs en attendant la résolution de l'incident.

08h12 - Virginie passe son billet 879277246472 possédant un QR code sur la [Badgeuse] 256
08h12 - Le [Système] interroge la base de donnée et renvoie OK.
08h12 - La LED de la [Badgeuse] 256 passe au vert
08h12 - La porte du côté de Virginie du [Bisas] correspondant s'ouvre
08h13 - Virginie entre dans le [Bisas]
08h13 - Anne entre dans le [Bisas]
08h13 - La porte ouverte du [Bisas] se ferme
08h13 - La LED du [Bisas] passe au orange
08h13 - Le Système détecte qu’il y a deux personnes à l’intérieur
08h13 - La LED du [Bisas] passe au rouge
08h13 - Le Système déclenche un [Incident]
