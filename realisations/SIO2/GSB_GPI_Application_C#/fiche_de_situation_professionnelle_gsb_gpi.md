# FICHE DE SITUATION PROFESSIONNELLE — BLOC 1 (ÉPREUVE E5)

## 1. IDENTIFICATION GÉNÉRALE

- **Titre de la réalisation :** GSB-GPI : Application de gestion du matériel et des incidents

- **Cadre de réalisation :** [ ] Stage 1  [ ] Stage 2  [ ] Atelier de professionnalisation  [X] Projet de cours

- **Période de réalisation :** Octobre / Novembre 2026

- **Modalité :** [ ] Individuel  [X] En équipe (3 collaborateurs : Nills Maillet, Karar Ali Hassan, Mattéo Dauriac)

- **Localisation / Organisation cliente :** Lycée Polyvalent et Technologique Henri Matisse / Laboratoire Galaxy Swiss Bourdin (GSB)

## 2. CONTEXTE ET OBJECTIFS

- **Contexte organisationnel :** Le laboratoire Galaxy Swiss Bourdin (GSB) compte plus de 500 collaborateurs répartis en métropole et outre-mer, disposant d'un parc informatique vaste et hétérogène (plus de 350 postes, tablettes, matériel en location). La gestion de l'inventaire et le suivi des incidents manquaient cruellement de centralisation et de traçabilité.

- **Problématique / Besoin exprimé :** GSB avait besoin d'une solution centralisée et unifiée pour fiabiliser la tenue de l'inventaire du matériel (postes, serveurs, équipements réseau, garanties, locations) et accélérer la prise en charge ainsi que la résolution des tickets d'incidents par les techniciens.

- **Objectifs fixés :**
  1. Centraliser et automatiser l'inventaire précis du parc informatique.
  2. Assurer un suivi complet des tickets d'incidents, depuis la déclaration initiale jusqu'à leur clôture.
  3. Mettre en place un contrôle d'accès rigoureux et dynamique selon le profil utilisateur (Utilisateur simple, Technicien, Responsable).

## 3. DÉMARCHE ET ENVIRONNEMENT TECHNIQUE

- **Environnement technologique mobilisé :**
  - Systèmes d'exploitation / Environnement : Windows, IDE JetBrains Rider (.NET 10.0)
  - Logiciels, frameworks et paquets : C#, Avalonia UI, Community Toolkit.Mvvm, Entity Framework Core, LINQ, PostgreSQL (hébergé sur Supabase), BCrypt, Figma, GanttProject, Notion, Git/GitHub.
  - Matériels ou éléments d'infrastructure concernés : Postes de travail, serveurs d'infrastructure, équipements réseau.

- **Démarche suivie étape par étape :**
  1. Analyse préalable, planification de projet (Gantt) et conception de l'architecture logicielle (MVVM) ainsi que des maquettes graphiques sur Figma.
  2. Modélisation des données (MCD, MLD) et mise en œuvre technique de la base de données PostgreSQL sur Supabase, couplée au développement des Models et de la classe centralisée d'accès aux données `DbToolBox`.
  3. Développement des vues AvaloniaUI, de la navigation par profils, des logs d'audit, puis compilation et publication de l'exécutable autonome en environnement de production.

- **Gestion des imprévus / Incidents rencontrés :** Des surcharges de travail ponctuelles ont été identifiées début novembre en raison du chevauchement de certaines tâches de développement, résorbées grâce à une forte coordination d'équipe via GitHub et l'espace Notion.

## 4. RÔLE ET CONTRIBUTION PERSONNELLE

- **Responsabilité précise :** En tant que membre actif de l'équipe de développement, ma mission s'est articulée autour de la co-conception architecturale et de la modélisation des données, puis de la prise en charge technique de la base de données et de l'intégration des services.

- **Actions menées individuellement :**
  - Participation active à la conception de l'architecture logicielle et de la maquette Figma.
  - Co-réalisation des modèles de données (Models) et des configurations de mapping avec Entity Framework Core.
  - Implémentation, structuration et sécurisation des méthodes d'interaction avec la base de données Supabase au sein de la classe `DbToolBox` (requêtes LINQ de sélection, insertion, modification, suppression et authentification sécurisée via hachage BCrypt).

## 5. LIVRABLES ET PREUVES ASSOCIÉES

- Schéma d'architecture MVVM et Diagramme des classes de l'application ([voir dans le rapport](./Rapport_GSB-GPI.md#conception-de-larchitecture-logicielle))
- Modèles conceptuel et logique de données (MCD & MLD validés) ([voir dans le rapport](./Rapport_GSB-GPI.md#conception-de-la-base-de-données-supabase))
- Extraits de code source de la classe `DbToolBox` et du contexte de données `GsbGPIDbContext` (gestion des requêtes LINQ et EF Core) ([voir dans le rapport](./Rapport_GSB-GPI.md#développement-de-la-base-de-données))
- Captures d'écran significatives de l'application finale (Écran d'authentification, Tableau de bord, Module de gestion des incidents et Module d'inventaire) ([voir dans le rapport](./Rapport_GSB-GPI.md#documentation-utilisateur))
- Procédure de compilation et livrable exécutable (`GSB-GPI.exe`) ([voir dans le rapport](./Rapport_GSB-GPI.md#compilation-du-projet))

## 6. COMPÉTENCES DU BLOC 1 MOBILISÉES

- [X] **B1.1 — Gérer le patrimoine informatique :** Recensement, suivi et structuration de l'inventaire complet du parc informatique (postes, serveurs, équipements réseau, garanties et conditions de location) au sein d'une base de données relationnelle centralisée.
  - *Preuves dans le rapport :* [Contexte et enjeux](./Rapport_GSB-GPI.md#contexte-et-enjeux), [Objectifs du projet](./Rapport_GSB-GPI.md#objectifs-du-projet), [Conception de la base de données Supabase](./Rapport_GSB-GPI.md#conception-de-la-base-de-données-supabase), [Développement des models](./Rapport_GSB-GPI.md#développement-des-models), [Mise en place de la base de données](./Rapport_GSB-GPI.md#mise-en-place-de-la-base-de-données), [Gestion de l'inventaire du matériel](./Rapport_GSB-GPI.md#gestion-de-linventaire-du-matériel-techniciens-et-responsables), [Objectifs atteints](./Rapport_GSB-GPI.md#objectifs-atteints) et [Script de sauvegarde PostgreSQL](./Rapport_GSB-GPI.md#script-de-sauvegarde-de-base-de-données-postgresql).

- [X] **B1.2 — Répondre aux incidents et demandes d'assistance :** Implémentation d'un module complet de création, d'assignation, de gestion des degrés d'urgence et de suivi des états de résolution des tickets pour les différents profils.
  - *Preuves dans le rapport :* [Périmètre fonctionnel et cahier des charges](./Rapport_GSB-GPI.md#périmètre-fonctionnel-et-cahier-des-charges), [Méthodes de la base de données](./Rapport_GSB-GPI.md#méthodes-de-la-base-de-données), [Développement des interfaces et de la navigation](./Rapport_GSB-GPI.md#développement-des-interfaces-et-de-la-navigation), [Déclaration et suivi d'un incident](./Rapport_GSB-GPI.md#déclaration-et-suivi-dun-incident-tous-profils), [Traitement des incidents](./Rapport_GSB-GPI.md#traitement-des-incidents-techniciens-et-responsable) et [Objectifs atteints](./Rapport_GSB-GPI.md#objectifs-atteints).

- [ ] **B1.3 — Développer la présence en ligne :** [Non mobilisé sur ce projet d'application lourde de bureau]

- [X] **B1.4 — Travailler en mode projet :** Utilisation d'un diagramme de Gantt prévisionnel et effectif, d'un espace collaboratif Notion, d'un versionnage Git/GitHub et répartition structurée des rôles au sein de l'équipe.
  - *Preuves dans le rapport :* [Équipe et répartition des rôles](./Rapport_GSB-GPI.md#équipe-et-répartition-des-rôles), [Démarche de gestion de projet](./Rapport_GSB-GPI.md#démarche-de-gestion-de-projet), [Outils de planification et de suivi](./Rapport_GSB-GPI.md#outils-de-planification-et-de-suivi), [Organisation du travail en équipe](./Rapport_GSB-GPI.md#organisation-du-travail-en-équipe), [Planification globale et diagramme de Gantt](./Rapport_GSB-GPI.md#planification-globale-et-diagramme-de-gantt), [Répartition de l'effort et des ressources](./Rapport_GSB-GPI.md#répartition-de-leffort-et-des-ressources), [Charge de travail et gestion des surcharges](./Rapport_GSB-GPI.md#charge-de-travail-et-gestion-des-surcharges), [Écarts entre le planning prévu et le déroulement réel](./Rapport_GSB-GPI.md#écarts-entre-le-planning-est-prévu-et-le-déroulement-réel) et [Difficultés rencontrées et enseignements](./Rapport_GSB-GPI.md#difficultés-rencontrées-et-enseignements).

- [X] **B1.5 — Mettre à disposition des utilisateurs un service informatique :** Conception d'une application de bureau ergonomique sous Avalonia UI, sécurisation rigoureuse des accès (BCrypt) et compilation d'un livrable autonome prêt pour le déploiement sur les postes clients.
  - *Preuves dans le rapport :* [Conception de la maquette Figma](./Rapport_GSB-GPI.md#conception-de-la-maquette-figma), [Développement des interfaces et de la navigation](./Rapport_GSB-GPI.md#développement-des-interfaces-et-de-la-navigation), [Développement des logs et création du logo](./Rapport_GSB-GPI.md#développement-des-logs-et-création-du-logo), [Compilation du projet](./Rapport_GSB-GPI.md#compilation-du-projet), [Documentation utilisateur](./Rapport_GSB-GPI.md#documentation-utilisateur) et [Administration des utilisateurs](./Rapport_GSB-GPI.md#administration-des-utilisateurs-responsable-uniquement).

- [X] **B1.6 — Organiser son développement professionnel :** Apprentissage et montée en compétences sur de nouvelles technologies (Avalonia UI, EF Core, Supabase, pattern MVVM) et rédaction d'une documentation technique et utilisateur complète.
  - *Preuves dans le rapport :* [Environnement technique et choix technologiques](./Rapport_GSB-GPI.md#environnement-technique-et-choix-technologiques), [Conception de l'architecture logicielle](./Rapport_GSB-GPI.md#conception-de-larchitecture-logicielle), [Phase de documentation](./Rapport_GSB-GPI.md#phase-de-documentation), [Bilan de la phase de documentation](./Rapport_GSB-GPI.md#bilan-de-la-phase-de-documentation), [Compétences acquises](./Rapport_GSB-GPI.md#compétences-acquises), [Perspectives d'évolution](./Rapport_GSB-GPI.md#perspectives-dévolution) et [Sources et références](./Rapport_GSB-GPI.md#sources-et-références).

## 7. BILAN RÉFLEXIF ET AUTO-ÉVALUATION

- **Points forts :** La rigueur apportée à la phase de conception (MCD, MLD, maquettes Figma) a grandement fluidifié le développement et garantit la cohérence globale de l'application. La centralisation des requêtes via `DbToolBox` et l'utilisation d'Entity Framework Core ont permis d'obtenir un code modulaire, maintenable et protégé contre les failles courantes comme les injections SQL.

- **Axes d'amélioration :** Une anticipation plus fine de la répartition de la charge de travail initiale aurait permis d'éviter les pics de surcharge au démarrage de la phase de codage. Sur le plan technique, l'externalisation des chaînes de connexion sensibles et l'activation de politiques de sécurité au niveau des lignes (RLS) sur Supabase constituent les priorités d'évolution.

- **Compétences professionnelles consolidées :** Maîtrise approfondie du pattern MVVM en C#, manipulation de bases de données distantes via LINQ et EF Core, bonnes pratiques de versionnement collaboratif et rigueur méthodologique en conduite de projet informatique.