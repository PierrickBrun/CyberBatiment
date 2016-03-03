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
