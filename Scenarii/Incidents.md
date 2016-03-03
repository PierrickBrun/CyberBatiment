Incidents
=========
Régler Piggybacking
------------

**Contexte** [Bruno] est gardien, [Bernardo] et [Marie] sont deux spectateurs qui sont entrés à deux
dans le même [Bisas] n°12 après avoir utilisé le billet de Marie. Le [Bisas] n°12 fait partie du
[PointAcces] n°5 menant à la Zone “Tribunes”, les tribunes du stade de Nilton Santos.

- Le driver du [Bisas] détecte la fermeture d’une de ses portes
- Le driver du [Bisas] détecte plus d’une personne dans le [Bisas]
- Le driver du [Bisas] renvoie le message “KO” signalant la détection de plus d’une personne dans le
SAS
- Le driver du [Bisas] fait passer la LED du [Bisas] au rouge
- Le [Bisas] se met en attente
- Le [ServeurControle] recoit le message “KO” en provenance du [Bisas] n°12
- Le [ServeurControle] transmet l’information au [ServeurApplicatif]
- Le [ServeurApplicatif] reçoit l’erreur
- Le [ServeurApplicatif] détermine que le [Bisas] n°12 fait partie du point d’accès n°5
- Le [ServeurApplicatif] détermine que le [PointAcces] n°5 permet d’accéder à la [Zone] “Tribune”
- Le [ServeurApplicatif] détermine que le [Gardien] chargé de la [Zone] “Tribune” est [Bruno]
- Le [ServeurApplicatif] génère un [IncidentSysteme] et l’envoie au Smartphone de [Bruno]
- Le [Gardien] en charge de la [Zone] “Tribunes” [Bruno] recoit sur son smartphone l’[Incident] avec
le numéro du [Bisas] posant problème.
- [Bruno] choisi l’option “Résoudre”
- L’incident est enregistré comme résolu
- Le [ServeurApplicatif] envoie l’instruction “Evacuer occupants” au [ServeurControle]
- Le [ServeurControle] commande l’ouverture de la porte du [Bisas] sur la face par laquelle [Marie] et
[Bernardo] sont entrés

Ignorer PiggyBacking
--------------------

**Contexte** [Bruno] est gardien, [Bernardo] et [Marie] sont deux spectateurs qui sont entrés à deux
dans le même [Bisas] n°12 après avoir utilisé le billet de Marie. Le [Bisas] n°12 fait partie du
[PointAcces] n°5 menant à la Zone “Tribunes”, les tribunes du stade de Nilton Santos.

- Le driver du [Bisas] détecte la fermeture d’une de ses portes
- Le driver du [Bisas] détecte plus d’une personne dans le [Bisas]
- Le driver du [Bisas] renvoie le message “KO” signalant la détection de plus d’une personne dans le
SAS
- Le driver du [Bisas] fait passer la LED du [Bisas] au rouge
- Le [Bisas] se met en attente
- Le [ServeurControle] recoit le message “KO” en provenance du [Bisas] n°12
- Le [ServeurControle] transmet l’information au [ServeurApplicatif]
- Le [ServeurApplicatif] reçoit l’erreur
- Le [ServeurApplicatif] détermine que le [Bisas] n°12 fait partie du point d’accès n°5
- Le [ServeurApplicatif] détermine que le [PointAcces] n°5 permet d’accéder à la [Zone] “Tribune”
- Le [ServeurApplicatif] détermine que le [Gardien] chargé de la [Zone] “Tribune” est [Bruno]
- Le [ServeurApplicatif] génère un [IncidentSysteme] et l’envoie au Smartphone de [Bruno]
- Le [Gardien] en charge de la [Zone] “Tribunes” [Bruno] recoit sur son smartphone l’[Incident] avec le numéro du [Bisas] posant problème.
- [Bruno] se déplace sur les lieux de l’incident
- [Bruno] constate un faux-positif, personne ne se trouve dans le [Bisas]
- [Bruno] choisi l’option “Ignorer” parmis les options sur son smartphone
- L’incident est enregistré comme ignoré sur le [ServeurApplicatif]
- Le [ServeurApplication] envoie une instruction au [ServeurControle] pour remettre en fonction de
[Bisas]
- Le [ServeurControle] envoie l’instruction “Remettre en fonction” au [Bisas]
- Le driver du [Bisas] le remet en fonction
