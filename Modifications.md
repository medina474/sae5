# Modifications du cahier des charges

A la suite d'une réunion avec les futurs utilisateurs il apparait un mode de fonctionnement "caché". L'ancien logiciel peu souple ne permetait pas d'effectuer certains ajustements. Des combines sont apparus pour pouvoir coller à la réalité.

## Modification du calendrier de livraison

Des formes de souplesse dans le calendrier de livraison sont parfois proposées aux clients afin de s'adapter à leurs absences.
Ainsi, pour chaque type d'abonnement, la structure doit pouvoir paramétrer les autorisations de modifications du calendrier de livraison qu'elle donne au client. Il existe les 2 cas suivants :

### 1er cas : report de livraison du produit

La structure offre la possibilité au client de modifier la semaine de livraison d'un produit prévu, aussi bien en anticipé avant la date prévue qu'en report après la date prévue. S'il y a déjà un produit de prévu en livraison sur cette semaine, le client en recevra donc 2.

Dans le cas d'un abonnement lié à une période déterminée, le report de livraison du produit ne peut se faire que dans la période de l'abonnement (on ne peut pas le reporter après la fin de période).

Dans le cas d'un abonnement lié à un nombre de produits à recevoir, il n'y a pas à priori pas de contrainte de période, cela peut être reporté dans le temps après la fin du calendrier initialement prévu. En revanche la structure peut choisir ou non de déterminer un nombre maximum de produits qui peuvent être reportés.

Il faudra pouvoir paramétrer un délai minimal dans le back-office pour éviter une annulation 2H avant la confection des paniers.

### 2ème cas : annulation de la livraison de produits

Ce cas ne concerne que les abonnements liés à une période déterminée.
La structure offre la possibilité au client de supprimer une ou plusieurs livraisons de produits de son abonnement. La livraison et le produit sont tous simplement déprogrammés, ils ne seront donc pas facturés au client (impact sur le solde / les règlements initialement prévus).

Dans le paramétrage de cette option, la structure doit pouvoir définir si elle le souhaite un nombre maximum d'annulations autorisées par abonnement.

Chaque structure peut choisir, pour chacun de ses abonnements, de proposer l'une, l'autre, les 2, ou aucune de ces formes de souplesse.

Les modifications du calendrier de livraison (reports ou annulation de la livraison d'un produit) peuvent être faits soit par le client en front office depuis son espace client, soit par les salariés de la structure en back office depuis le calendrier de livraison prévu pour ce client. Lors de cette opération de déclaration d'absence, l'outil doit vérifier sur l'ensemble du compte client s'il y a d'autres livraisons de produits de prévues sur cette même semaine d'absence (ex : abonnement panier + œuf + fromage) et offrir la possibilité d'effectuer les reports / annulations pour tous les produits ou individuellement pour chacun des cas.

Il est possible également qu'un client demande à changer de jour de livraison dans la semaine (ex : changer la livraison prévue le Mardi au Vendredi, ce qui peut impliquer un changement de point de dépôt).

## Paniers annulés, reportés

Fixer un nombre maxi de paniers annulés/reportés sur une période (ex : 3 paniers annulés/reportés maxi sur juillet et août). Mais l'adhérent peut faire une demande de « dérogation » si besoin de plus de 3 annulations : c'est alors l'admin, si d'accord, qui fait l'action d'annuler/reporter un 4ème, 5ème panier, en backoffice.

Le « doublage » des paniers doit pouvoir être contrôlé. ex : en été, nécessaire de répartir et étaler les paniers doublés, car impossible de doubler 50 paniers sur la dernière semaine d'août par exemple. Si liberté donnée aux adhérents de choisir les semaines où ils souhaitent doubler leurs paniers, risque d'avoir des semaines avec énormément de paniers doublés => ingérable niveau maraîchage. Donc mettre un compteur qui bloc lorsque le nombre max de paniers doublés et atteint.

- Mais pour garder une marge de manœuvre et flexibilité, admin doit pouvoir agir et ajouter des doublés en backoffice, pour modifier le quota maxi.
- Lorsque l'adhérent annule un panier, il doit donner une date de doublage obligatoirement pour compenser. Ou bien afficher un décompte (vous avez annulé 2 paniers cette année, et doublé 1 seul => vous avez un panier à doubler avant la fin de l'année)
- Fixer une date limite pour annuler/reporter/doubler un panier : max 48h avant !

## Changement de point de dépôt

L'ensemble des éléments de l'abonnement sont automatiquement programmés sur le même point de dépôt.

Néanmoins il est possible de changer de point de dépôt ponctuellement pour une date ou période précise, ou définitivement pour toute la fin de l'abonnement. Cela peut se faire en back office par les salariés de la structure ou en front office sur l'espace client par le client. Garder à l'esprit que certains PDD sont réservés à un public spécifique (la mention doit toujours apparaître + validation par mot de passe si ce type de PDD est choisi pour un changement).

Lors de cette opération de changement de PDD, l'outil doit vérifier sur l'ensemble du compte client s'il y a d'autres livraisons de produits de prévues sur ce PDD pour cette même date ou période (ex • abonnement panier + œuf + fromage) et offrir la possibilité d'effectuer les changements de point de dépôt pour tous les produits ou individuellement pour chacun des cas.
