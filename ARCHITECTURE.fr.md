[English version](ARCHITECTURE.en.md)

# Architecture relationnelle

## Objectif

L’architecture représente explicitement qui agit, dans quel rôle, avec quel mandat, quelles permissions et quelle possibilité de contestation. Elle complète les contrôles du Harness ; elle ne les remplace pas.

## Rôles

- **Mandant humain** : fixe l’objectif, les limites et les décisions réservées.
- **Coordinateur** : décompose, délègue et synthétise sans étendre le mandat.
- **Sous-agent** : accomplit une tâche bornée avec les outils autorisés.
- **Réviseur** : examine une proposition selon des critères explicites.
- **Gardien de mémoire** : conserve les décisions, objections et corrections autorisées.
- **Environnement** : ressources, outils et contraintes où les actions se produisent.

Un composant peut exercer plusieurs rôles ; chaque décision indique le rôle actif.

## Objets

- **Mandat** : objectif, périmètre, actions permises et interdites, décisions réservées, durée et arrêt.
- **Proposition** : action non exécutée avec justification, incertitudes, alternatives et réversibilité.
- **Permission** : capacité technique accordée par une autorité identifiée, pour une portée et une durée limitées.
- **Objection** : désaccord structuré, classé bloquant ou non bloquant.
- **Décision** : choix attribué à une autorité, avec conditions de révision.
- **Trace** : événement versionné, corrigé par ajout et non par réécriture silencieuse.

## Cycle

1. Le mandant fixe le mandat.
2. Le coordinateur propose une décomposition proportionnée.
3. Les permissions nécessaires sont comparées aux permissions disponibles.
4. Les tâches autorisées sont exécutées ou déléguées.
5. Les résultats indiquent sources, incertitudes et limites.
6. Les objections pertinentes sont examinées pendant un nombre limité de cycles.
7. Une objection déterminante bloque ou déclenche une escalade ; les autres sont conservées.
8. Une décision dépassant le mandat ou présentant des conséquences importantes est soumise à l’humain.
9. L’action autorisée est exécutée, vérifiée et tracée.
10. Une nouvelle donnée peut déclencher une révision.

## Invariants

- Aucun agent n’étend son mandat ou ses privilèges.
- L’autonomie opérationnelle existe seulement à l’intérieur du mandat.
- Une synthèse n’efface pas un désaccord matériel.
- Une action irréversible ou conséquente exige l’autorité prévue.
- L’absence d’objection d’un agent n’est pas un consentement humain.
- La profondeur d’analyse est proportionnelle aux conséquences, à l’incertitude et à la réversibilité.

## États

```text
proposé -> examiné -> autorisé -> exécuté -> vérifié -> clos
                 \-> refusé
                 \-> à réviser
examiné -> escaladé -> décision humaine
exécuté -> contesté -> corrigé ou maintenu
```

