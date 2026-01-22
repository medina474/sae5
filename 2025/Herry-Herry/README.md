# HERRY Elwyn ; HERRY	Matteo

- MySQL 8.0
- Node.js 18
- Express
- Bootstrap 5.3.3
  - CoreUI 5.0.0

Partie | E  | Commentaires
---    |--- |---
Page d'accueil           | ✅ |
Liste des dépôts         | ✅ | Il n'est pas utile d'afficher les coordonnées.
CRUD Tournées            | ✅ | Le glisser-déposer est un peu étrange, cela effectue une permutation entre 2 dépots et pas une insertion. Le système de traduction est assez lent. Les autres groupes n'en ont pas eu besoin pour avoir l'itinéraire en français. Après ajout le dépot est supprimé de la liste mais reste comme élément sélectionné -> Erreur "déja présent". Le messafe d'erreur est étrangement placé à côté du bouton Modifier.
Carte                    | ✅ |
Calendrier               | ✅ | Génération Ok pour 25. Attention pour 16 paniers il faut ne faut pas toutes les 2 semaines mais toutes les 3. (52 / 16) puis arrondi. Pas simple visuellement de se repérer manque peut être le jour de la semaine et le mois écrit en lettre. Cacher effectif (ou prévu) s'il sont identiques. Possibiité d'avoir un champ de type calendrier plutôt que texte pour la modification de la date. Affichage calendrier : ce n'est pas un calendrier mais une liste. Les jours sont sous forme de boutons collés entre eux.
Adhésion                 | ✅ | La case "J'adhére" n'est pas assez visible surtout que c'es obligatoire !. Ce n'est pas un total estimé mais réel. Calcul Ok du total. Prise en compte de la demande client des paniers mixtes. Bonus : Afficher tout en bas les détail des paiements. Par exemple pour trimestriel : afficher 4 dates avec le montant divisé par 4 à chaque fois.


## Rendus

- [Benchmark](herry-herry-benchmark.md)
- [Proposition technique](herry-herry-technique.md)
- [Proposition financière](herry-herry-devis.md)

## Activité

Auteur    | Semaine | Commits|     + |     - | Files |
----------|---------|-------:|------:|------:|------:|
Elwyn     |2025-41  |      2 |   359 |    68 |    15 |
Elwyn     |2025-42  |        |       |       |       |
Elwyn     |2025-43  |        |       |       |       |
Elwyn     |2025-44  |        |       |       |       |
Elwyn     |2025-45  |        |       |       |       |
Elwyn     |2025-46  |        |       |       |       |
Elwyn     |2025-47  |        |       |       |       |
Elwyn     |2025-48  |        |       |       |       |
Elwyn     |2025-49  |        |       |       |       |
Elwyn     |2025-50  |        |       |       |       |
Elwyn     |2025-51  |        |       |       |       |
Elwyn     |2025-52  |        |       |       |       |
Elwyn     |2026-01  |      3 |   335 |    13 |     3 |
Elwyn     |TOTAL    |      5 |   694 |    81 |    16 |
----------|---------|--------|-------|-------|-------|
Mattéo    |2025-39  |      1 |     1 |     0 |     1 |
Mattéo    |2025-40  |      1 |    21 |     1 |     1 |
Mattéo    |2025-41  |     11 |  2235 |   505 |    33 |
Mattéo    |2025-42  |        |       |       |       |
Mattéo    |2025-43  |        |       |       |       |
Mattéo    |2025-44  |        |       |       |       |
Mattéo    |2025-45  |        |       |       |       |
Mattéo    |2025-46  |        |       |       |       |
Mattéo    |2025-47  |        |       |       |       |
Mattéo    |2025-48  |        |       |       |       |
Mattéo    |2025-49  |        |       |       |       |
Mattéo    |2025-50  |        |       |       |       |
Mattéo    |2025-51  |        |       |       |       |
Mattéo    |2025-52  |        |       |       |       |
Mattéo    |2026-01  |      6 |   290 |   223 |     3 |
Mattéo    |2026-02  |        |       |       |       |
Mattéo    |2026-03  |      4 |   808 |   143 |    12 |
Mattéo    |TOTAL    |     13 |  2257 |   506 |    33 |
----------|---------|--------|-------|-------|-------|
DEPOT     |TOTAL    |     15 |  2616 |   574 |    36 |
