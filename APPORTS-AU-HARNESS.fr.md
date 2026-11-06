[English version](CONTRIBUTIONS-TO-THE-HARNESS.en.md)

# Apports possibles au Harness multi-agent

## Proposition, pas état vérifié

Ce document décrit des apports conceptuels. Aucun audit du code local du Harness n’a été réalisé pour cette finalisation. Les fonctions réellement disponibles, leurs permissions et leur comportement doivent être vérifiés séparément avant implémentation.

## Apports

- **Mandat attaché à la délégation** : objectif, résultat, interdits, outils, sources, arrêt et escalade.
- **Provenance** : chaque élément important de synthèse relié à sa source et à son agent.
- **Objections structurées** : bloquantes ou non bloquantes, sans consensus artificiel.
- **Permissions logiques bornées** : mandat plus étroit que l’exposition technique éventuelle des outils.
- **Points de décision humaine** : publication, écriture externe, dépense, suppression, changement de permission et décision conséquente.
- **Mémoire de révision** : comparaison entre ancienne et nouvelle décision lorsque les prémisses changent.
- **Résultats négatifs** : conservation des échecs pertinents pour éviter leur répétition.

## Action proportionnée

Le coordinateur agit dans le mandat sans demander une validation répétitive pour chaque opération faible risque déjà autorisée. Il limite les cycles d’objection et escalade uniquement ce qui dépasse le mandat, produit des conséquences importantes ou révèle une contradiction déterminante.

## Limites

Plusieurs agents ne sont pas nécessairement indépendants. Une synthèse peut ajouter des erreurs. Un environnement partagé peut créer des conflits. L’héritage d’outils n’est pas l’héritage d’autorité. Une approbation automatisée ne remplace pas la gouvernance humaine pour les décisions réservées.

## Première implémentation proposée

Prototype local sur données synthétiques, limité à Observer, Analyser et Préparer. Tester d’abord mandat, objections, mémoire A/B/C et révision. Ne connecter aucune action externe avant validation des critères, des contrôles et des arrêts.

