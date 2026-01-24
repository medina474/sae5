# Rendu 16 : Développement Back-office 2a

- **Étudiants concernés :** formation initiale parcours insertion professionnelle

Concevoir l'interface permettant de spécifier les plannings de livraison en fonction de la tournée et du nombre de panier à livrer.

L'administrateur choisi :

- l'année (ou par défaut l'année en cours)
- Le nombre de panier à distribuer (correspondant à la fréquence : 25 paniers pour livraison tous les 15 jours. Mais dans l'absolu cela peut être n'importe quel nombre)
- Le jour de livraison : Par exemple mercredi
- La tournée (Il se peut que deux tournées du même jour ne partage pas le même calendrier. Par exemple mercredi matin et mercredi après midi)

1. Le système calcul le placement des jours de livraison en évitant les semaines de fermeture et les jours fériés. Il faut  demander lors de la génération si le départ est une semaine paire ou impaire.
2. L'administrateur a la possibilité de déplacer des jours (Exemple le 1er mai a été décalé automatiquement au 2 mais l'utilisateur préfère peut être le 30 avril)
3. Le système vérifie avant validation que les x paniers sont tous placés (pas de surplus ni de manque)

Attention une livraison du vendredi ne peut pas être décalée au samedi c'est obligatoirement le jour avant. Et le lundi ne peut pas être décalé au dimanche c'est obligatoirement le jour après.

Vérifier l'algorithme avec 25, 20 et 17 paniers.

## Documents fournis

- [Planning du mardi](plannings/Planning%20mardi.pdf)
- [Planning du mercredi](plannings/Planning%20mercredi.pdf)
- [Planning du vendredi](plannings/Planning%20vendredi.pdf)
- [Exemple d'interface](planning/Planning.pdf)

## Nouveauté 2026

Mettre en place un test unitaire qui vérifie les conditions suivantes :
