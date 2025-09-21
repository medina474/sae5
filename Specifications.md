# Cahier des charges

Un Jardin de Cocagne est une association composée de salariés permanents constituant l'équipe d'encadrement, de salariés en réinsertion professionnelle (chômeurs de longue durée, personnes en très grande difficulté sociale, réfugiés, détenu en liberté conditionnelle, etc.) et d'adhérents consommateurs.

Seuls les adhérents peuvent utiliser les services de l’association.

Les adhérents peuvent s'abonner à des paniers, de différentes tailles et composition.

Ces paniers sont livrés à des fréquences régulières (toutes les semaines, toutes les deux semaines, tous les mois) dans des dépôts. Les adhérents viennent chercher leurs paniers dans le dépôt.

Le système informatique devra comprendre un backoffice utilisé par l'équipe du Jardin pour gérer les abonnements et les livraisons et d'un frontoffice permettant aux adhérents de suivre leurs abonnements.

- [Brochure de présentation 2023](presentation/brochure-2023.pdf)
- [Brochure de présentation 2024](presentation/brochure-2024.pdf)

___

> [!WARNING]
> Ce document est un cahier des charges original donné par une structure nationale en vue de développer un système complet de gestion. Il vous expose à une mise en situation réelle. Il ne définit pas les priorités de développement, ni le rendu attendu pour cette situation d'apprentissage et d'évaluation. Quelques références au logiciel Dolibarr sont présentes dans ce document. Cette solution n'est finalement pas retenue et doit être ignorée.

### Objectifs du document

Ce document représente un cahier des charges pour la réalisation du futur logiciel de **gestion commerciale** des Jardins de Cocagne.

Il doit servir de base à la rédaction d'une proposition **technique** et **financière** de développement et de déploiement de ce logiciel.

Ce projet doit répondre à 2 enjeux majeurs pour le Réseau et les Jardins de Cocagne.

- doter les jardins de cocagne d'un outil qui favorise le développement de leur activité économique mais aussi à terme les relations avec leur communauté d'adhérents et de partenaires économiques,
- constituer un projet co-pensé et co-construit par les jardins de cocagne et non pensé par la tête de réseau au bénéfice de ses membres.

## 1. Structure

Un module de paramétrage initial doit permettre de saisir les données de la structure utilisatrice :

- Logo de la structure
- Nom commercial
- Raison sociale
- Siège social
- Adresse de gestion
- Coordonnées commerciales : téléphone, mail, nom éventuel de la personne de contact, site web
- N° de SIRET
- Coordonnées bancaires de la structure : BIC, IBAN, n° ICS
- Une case à cocher « structure assujettie / non assujettie à la TVA »

### Quelques structures

- [Jardins de Cocagne de Thaon-les-Vosges](https://thaonlesvosges.fr/ville-au-quotidien/emploi/les-structures-de-linsertion-par-lactivite-economique/les-jardins-de-cocagne/)
- [Le jardin de Cocagne Angevin](https://www.jardin-cocagne-angers.org/)
- [Les potagers de Velles](https://www.solidariteaccueil.org/les-potagers-de-velles)
- [Oasis](https://oasis.bio/index.php/paniers-bio/)
- [Lille](https://www.jardindecocagne-lille.org/content/23-je-decouvre)
- [Le jardin d'Ethan](https://jardindethan.fr/casier-en-libre-service/)
- [Graine de Cocagne](https://grainedecocagne.cocagnebio.fr/)
- [Jardin Julienne Javel](https://www.cocagneabonnement.org/paniers-de-legumes/)
- [Jardin de Macon](https://jdcmacon.org/contenu-des-paniers/)

## 2. Saisons

L’application doit permettre de définir et gérer la notion de **saison**, correspondant à l’année associative propre à chaque structure.

La saison représente la période de référence pour la vie de l’association : elle encadre la gestion des adhésions, des cotisations et des activités collectives (ex. : répartition des parcelles, organisation des livraisons, planification des fermetures).

Chaque saison est caractérisée par :

* une **date de début** et une **date de fin** (qui peuvent différer de l’année civile),
* la possibilité d’indiquer des **semaines de fermeture** ou **jours fériés** sans activité,
* un **libellé** permettant d’identifier facilement la saison (ex. : « Saison 2025 », « Printemps–Hiver 2026 », etc.).

La gestion multi-saisons doit être possible afin de conserver l’historique et de préparer la saison suivante tout en clôturant la précédente.

La structure doit définir de manière générale son calendrier livrable c'est-à-dire les jours et semaines où des livraisons sont possibles.

### 2.1 Semaines non livrables

La structure doit pouvoir définir, de manière globale les **semaines non livrables**, à cocher sur un calendrier.

### 2.2 Jours fériés

La prise en compte des **jours fériés** auront pour incidence de **décaler** la livraison sur un jour inhabituel de la même semaine (ex : mardi 8 mai férié, livraison décalée au mercredi 9 mai). Cette déclaration des décalages de livraison doit s'aborder jour férié par jour férié, et idéalement par tournée de livraison (exemple pour 2 tournées prévues les mardis, l'une pourrait être décalée au lundi et l'autre au mercredi pour des raisons d'organisation).

## 3. Dépôts

> [!NOTE]
> Les dépôts sont des lieux de livraison des produits commandés. Ils regroupent la plupart du temps plusieurs commandes, que les clients viennent chercher à cet endroit à un **jour** et **créneau horaire** précis.

Une fiche point de dépôt comprend :

- N° identifiant créé automatiquement (numéro unique, non modifiable)
- Identifiant de tournée et no d'ordre de livraison dans la tournée (cf. « [Tournée de livraison](#5-tournées-de-livraison) »).
- Nom du point de dépôt, adresse, code postal, ville, no de téléphone n° obligatoire pour l'enregistrement de la fiche
- Mail générique de la structure, site web de la structure (facultatif)
- Nom de la personne référente + mail + téléphone spécifique de la personne référente
- On doit pouvoir préciser le jour de livraison de ce point de dépôt (incidence sur la commande et la feuille de route), le créneau horaire de livraison (information interne) et les créneaux horaires de récupération des paniers (apparaîtront en front office).
- Une zone de texte libre de présentation du lieu et le téléchargement possible d'une photo ou image du lieu.
- Prévoir une case de texte libre pour noter des commentaires.

### 3.1 Capacité d'accueil

Prévoir une case permettant de définir le nombre d'abonnements paniers maximum accueillis sur le point de dépôt. Cela induirait ensuite une fonction de vérification du nombre de places restantes pour valider une nouvelle inscription, et pourra définir un statut COMPLET de point de dépôt.

La capacité d'accueil doit être affichée dans l'espace d'information.

### 3.2 Catégories

Prévoir 3 catégories de points de dépôts à choisir en menu déroulant :

#### Dépôts ouverts à tous

ex : cas d'une boulangerie où n'importe qui peut se faire livrer un panier Ces PDD sont disponibles et affichés en tous lieux du front office.

#### Dépôts réservés à un public spécifique

ex : cas d'un comité d' entreprise ou seuls les salariés de l'entreprise peuvent s'y faire livrer un panier Ces PDD sont affichés publiquement sur le front office mais indiquent une petite phrase « réservé aux ... (texte personnalisable) ». Ils sont proposés dans le parcours de commande, mais le choix de ce PDD est soumis à validation par un mot de passe.

En back office, sur les fiches PDD appartenant à cette catégorie, on doit avoir une case où écrire le texte personnalisable et une case avec le mot de passe (unique et modifiable).

L'information « Point dépôt réservé aux texte personnalisable » si c'est un PDD Réservé à un public spécifique

Cette information doit être affichée dans l'espace d'information.

#### Dépôts professionnels

ex : cas d'une école qui commande des légumes pour sa cantine
En back office, sur les fiches PDD appartenant à cette catégorie, on doit pouvoir lier le lieu à une catégorie de client (cf. « 3.2 Clients »). En front office, ces PDD Professionnels n'apparaissent pas sur le site général, et n'apparaissent que dans le parcours de commande privé depuis les espaces clients des personnes appartenant à cette catégorie de client (cf. « 3.11 Parcours de Commande »).

Les catégories doivent s'afficher de manière différente sur la carte de localisation.

Sur la carte publique, ne doivent figurer que les PDD ouverts à tous et ceux réservés à un public spécifique (n'apparaissent pas les PDD professionnels). Dans les commandes des professionnels (catégories clients spécifiques), un onglet déroulant des PDD de leur catégorie sera suffisant si c'est plus simple.

Il serait pertinent que les indicateurs des points de dépôts puissent avoir une couleur différente : 1 couleur pour l'indicateur du PDD sur le site du Jardin de Cocagne, 1 couleur pour les PDD ouverts à tous, 1 couleur pour les PDD réservés à un public spécifique.

## 4. Jours de préparation

Les jours de préparation sont des jours pendant lesquels tous les paniers appartenant à une ou plusieurs tournées sont préparés.


## 5. Tournées de livraison

Les points de dépôts sont livrés dans des **tournées de livraison**.

Une tournée de livraison est définie par :

- un identifiant de tournée qui doit pouvoir être personnalisable (chiffre ex : 1, 2, 3 ; ou lettre ex : tournée Ma ou V pour Mardi ou Vendredi, ou tournées BLR ou MTR pour Beaune la Rolande ou Montrouge.)
- un jour de livraison
- une **succession ordonnées** de points de dépôts, définie grâce à un n° d'ordre de livraison dans la tournée, donner la possibilité de définir une couleur pour une tournée (la couleur a pour incidence de coloriser les PDD dans la partie gestion des PDD et synthèse des commandes à préparer et livrer / feuilles de route)

(Planning du mercredi)[plannings/Planning%20mercredi.pdf]

## 6. Adhérents

Un client peut être une personne physique ou morale.

La fiche client comporte :

### 6.1 les éléments relatifs à son identité.

- N° identifiant créé automatiquement (numéro unique, non modifiable)
- Raison sociale (en cas de personne morale)
- Civilité (Mr / Mme...). Prévoir un onglet déroulant avec le contenu paramétrable dans les initialisations
- Nom, Prénom, Adresse, Code Postal, Ville, n° téléphone, mail. Rendre ces éléments obligatoires pour l'enregistrement de la fiche.
- 2ème et 3ème case de téléphone, Profession, date de naissance. Éléments facultatifs pour l'enregistrement de la fiche
- Mot de passe d'accès à son espace client « Mon compte » (créé automatiquement mais modifiable)

### 6.2 Les éléments relatifs à son adhésion

- Date de 1ère adhésion,
- Historique des adhésions avec leur période et le type d'adhésion.
- Élément indiquant si l'adhésion est à jour ou non (réglée ou non réglée / en cours ou expirée), avec indication de la date d'expiration de la dernière adhésion.
- Une case « dispensé d'adhésion » à cocher, pour le cas de clients professionnels à qui l'on ne demande pas d'adhésion.

Pour le reste [cf. le paragraphe 7](#7-adhésions)

### 6.3 Les éléments relatifs à ses différentes commandes de produits ou d'abonnements

- Les commandes doivent pouvoir être réalisées, modifiées, ou visualisées depuis la fiche client. L'historique des commandes doit être présent, avec l'information du point de dépôt et les frais de livraison éventuellement associés, et un accès aux bons de livraisons et aux factures.

> Note : Il se peut qu'un client ait plusieurs abonnements en même temps (pas de limite de nombre).

Pour le reste cf le paragraphe 8

## 7. Adhésions

> [!NOTE]
> Il sera nécessaire de distinguer l'adhésion à l'abonnement panier et l'adhésion à l'association Jardin de Cocagne avec la possibilité de lier automatiquement les deux dans le paramétrage de la structure.

Les deux sont liés, un adhérent panier est obligatoirement adhérent de l'association (l'inverse n'est pas vrai).

Un adhérent sans panier est appelé un **soutien**. Il devra être dans la liste des personnes convoquées aux assemblées générales de l'association.

### 7.1 Adhésion à l'association

> [!NOTE]
> A noter que c'est cette adhésion qui est la base pour calculer une partie de la cotisation annuelle que reverse le jardin au Réseau national.

Dans le cas des Jardins de Cocagne sous statut associatif (98 % des jardins), l'adhésion est obligatoire pour pouvoir accéder aux services et à la vente des produits de l'association. Tout client doit avant tout être adhérent, sauf cas particulier de clients professionnels à qui l'on ne demanderait pas d'adhésion (cf. case « dispensé d'adhésion » prévue sur la fiche client).

On peut proposer différents types d'adhésion à des prix différents (exemple Adhésion soutien, Adhésion solidaire… ) qui doivent être paramétrables dans l'outil : libellé + montant.

les adhésions sont valables sur une périodicité fixe déterminée par le Jardin.

La périodicité doit être paramétrable dans l'outil. ex : année civile 01/01 au 31/12, ou bien du 01/04 au 31/03.

En général, une adhésion prise en cours de période est facturée à plein tarif, et est valable jusqu'à la fin de la période en cours.

Les renouvellements d'adhésions sont tous appelés en même temps, avant la fin de la périodicité fixe.


## 8. Produits

Les produits sont les différentes unités élémentaires qui peuvent être vendues. Cela peut être :

- des produits alimentaires (légumes, fruits, pain, œuf, ...) qui disposeront chacun d'une unité appropriée (pièce, kg, botte, filet, boîte, bouteille, colis)
- des lots composés de différents produits (ex : petit ou grand panier légumes, panier fruits, panier fermier . ou encore « composition ratatouille », « composition pot au feu » .
- des produits non alimentaires, matériels ou immatériels (ex : agenda, ecocup, adhésion, bon cadeau . . .)

id|produit|prix|marge
--:|---|--:|---
1|Panier simple  |13.80|40 %
2|Panier familial|23.70|40 %
3|Panier fruité 1|14.00|70 %
4|Panier fruité 3|23.00|70 %
5|Panier fruité 2|17.00|70 %
6|Oeufs x6       | 3.05|50 %
7|Panier fruité entreprise|23.50|70 %

## 9. Abonnements / Panier

Un abonnement est un pack de vente d'un même produit livré régulièrement. Les abonnements peuvent concerner tous les types de produits : aussi bien les produits élémentaires (ex : abonnement boîtes d'œufs), que les lots de produits (ex : abonnement au panier fermier). C'est à la structure de déterminer les abonnements qu'elle propose.

### 9.1 Durée d'un abonnement

L'abonnement est lié à une période déterminée.

La structure définit la période type de l'abonnement grâce à des calendriers (ex : sur l'année civile, par trimestre, de Mai à Octobre. ..). Tout abonnement pris est paramétré jusqu'à la fin de la période. Un abonnement peut être démarré en cours de période et va jusqu'à la fin de la période, un calcul est donc fait sur le nombre de produits restant à recevoir d'ici la fin de la période.

### 9.2 Fréquence
