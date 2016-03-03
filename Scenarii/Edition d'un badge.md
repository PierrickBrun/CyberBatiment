Editer un badge
==========================================
Définir une autorisation
------------------------

**Intention** [CyberCompetition] est en mesure de communiquer avec l’ERP interne [CyberBatiment] Pour la vente de billets pour le Stade de Nilton Santos

**Contexte** Il existe un [Groupe] “Hockey16012015” dédié à la compétition ayant lieu le 16/01/2017 de 12h à 17h donnant accès au stade dans les horaires de la compétition

- Un billet pour le Stade de Nilton Santos à été vendu pour la compétition qui aura lieu le 16/01/2017
de 12h à 17h sur la plateforme [CyberCompetition]
- Le serveur de [CyberCompetition] envoie une requète à l’[APIBillets] respectant le format normalisé par l’ERP [CyberCompetition] et contenant les - informations suivantes: Nom du groupe
“Hockey16012015”, Nom du spectateur “Virginie Maris”, Code correspondant au QRCode généré.
- Le [ServeurApplicatif] recoit et interprète l’information reçue
- Le [ServeurApplicatif] enregistre numéro du billet dans le [Groupe] “Hockey16012015”


Passage non autorisé
--------------------

**Contexte** Virginie est visiteuse, elle vient voir l'épreuve de ski nordique le 17/08/16 au stade de
Nilton-Santos à Rio. Elle se trompe de Billet et essaie de réutiliser celui de la veille lui permettant de
voir le triple saut.

- Virginie passe son billet 879277246472 possédant un QR code sur la [Badgeuse] 128, à 10:57
- Le [ServeurControle] reçoit la demande d’accès
- Le serveur de contrôle demande au [ServeurApplicatif] si le [Badge] 879277246472 est autorisé à
accéder à la [Zone] couverte par la [Badgeuse] 128 le 17/08/16 à 10:57
- Le [ServeurApplicatif] interroge la base de donnée et renvoie KO.
- Le [ServeurControle] renvoie KO à la [Badgeuse] et au [Bisas]
- La LED de la [Badgeuse] 128 passe au rouge
- Virginie ne peut pas pénétrer dans la [Zone] de l’épreuve


Passage avec piggybacking
-------------------------

**Contexte** Virginie est visiteuse, elle vient voir l'épreuve de triple saut le 16/08/16 au stade de
Nilton-Santos à Rio. Anne essaie de passer dans le [Bisas] avec Virginie pour économiser un Billet.

- Virginie passe son billet 879277246472 possédant un QR code sur la [Badgeuse] 256, à 10:52
- Le [ServeurControle] reçoit la demande d’accès
- Le serveur de contrôle demande au [ServeurApplicatif] si le [Badge] 879277246472 est autorisé à
accéder à la [Zone] couverte par la [Badgeuse] 256 le 16/08/16 à 10:52
- Le [ServeurApplicatif] interroge la base de donnée et renvoie OK.
- Le [ServeurControle] renvoie OK à la [Badgeuse] et au [Bisas]
- La LED de la [Badgeuse] 256 passe au vert
- La porte du côté de Virginie du [Bisas] correspondant s'ouvre
- Virginie entre dans le [Bisas]
- Anne entre dans le [Bisas]
- La porte ouverte du [Bisas] se ferme
- Le [Bisas] détecte qu’il y a deux personnes à l’intérieur
- Le [Bisas] prévient le [ServeurControle] pour qu’il déclenche un [Incident]
