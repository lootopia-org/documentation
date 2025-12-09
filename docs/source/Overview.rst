Overview
===

Problèmes identifiés
--------------------
ceci sont les problems que cette application devrai resoudre, cette application devrai etre simple, ludique et immersive, ca doit etre 1utilisable par des jouers, partenaires et admins:

- Applications de gamification trop limitées (quiz, géocaching uniquement), 
  - ceci devrai etre evidant, pour l'application on va utilser tous ce qui est RA pour etre capable de cree le jeu

- Expériences peu intuitives, surtout sur mobile.
  - pour ca on va suivre a maxmime les principales et standards de development mobile en ui et ux Test hyperlink: `ui guidelines to follow <https://www.smashingmagazine.com/2011/07/seven-guidelines-for-designing-high-performance-mobile-user-experiences/>`_.

- Peu d’outils pour les partenaires (musées, villes, associations).
  - pour ce point la on va cree une comprehensives partenaire dashboard qui contindra tous les fonctionalite que les partenaires aura besoin

- Intégration de la réalité augmentée marginale et complexe.
  - on va utilser les lib RA pour mettre en place du RA je pense surtout a utilse:
    - `A-Frame <https://aframe.io/>`_.
    - `AR.js <https://ar-js-org.github.io/AR.js-Docs/>`_.

Objectif du project
-------------------
il faut offrire une experiance fluide et intuitive aux utiltisateurs, peu importe que ca sois sur mobile ou web,
les partenaires doit etre capable de cree et gereer leurs proprs chasse, les jouers doit etre attire de jouer en utilsant la system
de gamefication(scores, progresion, reward), et au finale etre capable d'interagire ave le mode reel envers leurstelephone en utilsant la RA

.. list-table::
   :widths: 25 35 40
   :header-rows: 1

   * - Pôle
     - Besoins spécifiques
     - Exemples de solutions

   * - Utilisateurs
     - Créer compte, se connecter, rejoindre chasse
     - Auth JWT, formulaires simples

   * - Partenaires
     - Créer chasses, gérer étapes et indices
     - Backoffice minimal, CRUD

   * - Technique
     - API fiable, gestion DB, carto/RA
     - Node.js + PostgreSQL, Google Maps API, AR.js

   * - Direction
     - Produit démontrable et attractif
     - MVP, vidéo démo

Fonctionnalités attendues
-------------------------
1. Gestion utilisateurs : inscription, connexion, profils, auth sécurisée
2. Création et gestion de chasses (CRUD)
3. Participation aux chasses : carte interactive, points de passage, action Creuser.
4. Réalité augmentée basique : marqueurs AR via AR.js ou A-Frame
5. Gamification basique : progression et points
6. Interface intuitive et responsive

Innovations possible:
---------------------
1. Cartographie et RA mises en avant
2. Interface mobile first
3. Code modulaire pour extensions futures
4. Accessibilité et ** *UX respectées* **

Livrables
---------
- Analyse du besoin
- MVP fonctionnel (comptes, chasses, RA simple)
- Documentation technique (API, DB, architecture)

Kick Off
^^^^^^^^
Calendrier
~~~~~~~~~
Début d’année

Objectif
~~~~~~~~
Présentation de l’objectif du projet et du sujet et constitution des groupes

Conseils
~~~~~~~~
Visez la complémentarité des expertises dans vos groupes.

Video & MVP
^^^^^^^^^^^

Calendrier 
~~~~~~~~~~
Kick off + 6 mois

Objectifs
~~~~~~~~~
Créer une vidéo professionnelle de 15 à 20 min à destination du client, montrant une
démonstration du MVP (fonctionnalités implémentées, qualité du code, déploiement).

Modalités
~~~~~~~~~
- Présentation du projet au client
- Screencast de la solution, prise de parole de chaque membre (avec nom affiché), structuration
  claire (besoin → solution → démo).
- Tous les participants du projet doivent parler et un affichage doit apparaitre avec le nom de la
  personne au minimum

Livrables attendus
~~~~~~~~~~~~~~~~~~
Vidéo .MP4 ou lien vers vidéo youtube en mode non publié.

Forme du livrable
~~~~~~~~~~~~~~~~~
Solution 1 : Un fichier Zip contenant la vidéo du groupe.

- Nomenclature du zip :
  PE_2526_codepromo(ex : M1DEVA)_nometudiant1_nometudiant2_nom(etc…).zip

- Nomenclature de la vidéo :
  PE-2526_codepromo_NomPrenomEtudiant.mp4

**OU**

Solution 2 : Un document TXT contenant le lien vers la vidéo du groupe.
  
- A héberger sur youtube en mode Non Répertoriée. Toute autre plateforme ne sera pas
    validée.

- Nomenclature du document :
  PE_2526_codepromo(ex : M1DEVA)_nometudiant1_nometudiant2_nom(etc…).txt


Plan
~~~~

- Présentation de l'entreprise et de l'équipe projet
- Analyse de la problématique et introduction à la solution proposée
- Organisation et méthodologies appliquées
- Présentation de la solution technique

Conseils: répétez, soignez le son et les visuels, valorisez la pertinence de vos choix techniques.


Document technique finale
^^^^^^^^^^^^^^^^^^^^^^^^^
Calendrier
~~~~~~~~~
Kick off + 6 mois


Objectifs
~~~~~~~~~
Livrer un projet complet, industrialisable, documenté et testé.

Modalités
~~~~~~~~~
Code versionné avec branches propres, DAT, documentation d’installation, scripts
automatisés

Exemples de livrables attendus en fonction du projet :
- Backlog
- Justification des choix et anticipation des contraintes de performance et de déploiement
- Diagramme de Gantt
- Contributions individuelles détaillées
- DAT
- Code source + scripts tests/déploiement
- Gestion des coûts (M2)
- Documentation technique

Forme du livrable
~~~~~~~~~~~~~~~~~
Un fichier Zip contenant un rendu groupe (pdf) et un rendu par membre du groupe (voir plan).
- Nomenclature du zip :
  PE_2526_codepromo(ex : M1DEVA)_nometudiant1_nometudiant2_nom(etc…).zip

- Nomenclature du document groupe :
  PE-2526_codepromo_ nometudiant1_nometudiant2_nom(etc…).pdf

- Nomenclature des documents apprenants :
  PE-2526_codepromo_NomPrenomEtudiant.pdf

Plan
~~~~
Rendu groupe
~~~~~~~~~~~~
- Présentation de l'entreprise et de l'équipe projet
- Analyse de la problématique et introduction à la solution proposée
- Gestion des coûts et système économique (M2)
- Organisation de l’équipe, planification détaillée et méthodologies appliquées
- Présentation de la solution technique
- Conduite du changement (CPIT)

Rendu individuel
~~~~~~~~~~~~~~~~
- Perspectives d'évolution et réflexion sur l’avenir de l’infrastructure ou de la solution
  proposée
- Analyse critique sur les limites techniques rencontrées

Conseils : vérifiez la cohérence de la documentation, relisez-vous, préparez un bilan objectif.
