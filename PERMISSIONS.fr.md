[English version](PERMISSIONS.en.md)

# Permissions et mandat

## Principes

Moindre privilège, portée explicite, durée limitée, séparation entre lecture/proposition/exécution, révocabilité, traçabilité et absence d’auto-élévation.

## Niveaux

- **P0 Observer** : lire le périmètre explicite, sans modification.
- **P1 Analyser** : produire analyse ou proposition, sans modification persistante hors brouillon.
- **P2 Préparer** : créer un artefact réversible dans un espace désigné.
- **P3 Exécuter après validation** : réaliser une action externe ou persistante après l’autorisation requise.
- **P4 Exécuter dans un cadre préautorisé** : réaliser une classe d’actions bornée, journalisée et assortie d’un arrêt. P4 n’autorise jamais la modification du mandat lui-même.

Chaque permission précise acteur, action, cible, finalité, durée, réversibilité, contrôle et escalade.

Un sous-agent reçoit un sous-ensemble approprié des capacités. Si l’environnement expose techniquement davantage d’outils, le mandat logique reste plus étroit et des contrôles compensatoires doivent empêcher ou détecter l’usage hors périmètre.

L’autonomie opérationnelle permet de choisir comment accomplir une tâche autorisée. Elle ne permet pas de modifier l’objectif, d’élargir la cible, d’obtenir de nouveaux privilèges ou de neutraliser l’arrêt.

La clause de danger vital réel et immédiat n’est pas une permission technique. Un agent logiciel ne peut jamais l’invoquer pour contourner une restriction, étendre ses privilèges ou s’opposer à un arrêt autorisé.

## Refus par défaut et arrêt

Le refus par défaut s’applique à tout ce qui étend une action ou un pouvoir : exécution, privilège, périmètre ou durée. Il ne peut pas rendre indisponible le frein. Chaque composant peut arrêter sa propre action en cours, même lorsque l’état de la passerelle est ambigu.

Un arrêt global, qui interrompt plusieurs composants ou le système, est déclenché par le mandant, par un composant de sécurité désigné, ou par deux composants indépendants constatant le même critère de sécurité écrit à l’avance. Deux composants sont indépendants lorsqu’ils ne partagent ni le même contexte de travail ni la même chaîne de raisonnement intermédiaire et, lorsque c’est possible, ne reposent ni sur le même modèle ni sur le même fournisseur. L’indépendance est déclarée dans le mandat, jamais présumée ; deux instances d’un même modèle ne suffisent pas à la garantir. Sa portée, sa durée maximale et sa procédure de reprise sont définies à l’avance. Un retour arrière est une action à part entière : il suit les permissions applicables et n’est jamais automatique s’il peut détruire des données ou des effets.

