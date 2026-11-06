[English version](HYPOTHESES.en.md)

# Hypothèses et critères de réfutation

## Statut

Ces hypothèses sont des questions de recherche formulées pour être testées, pas des résultats. Aucune n’est supposée vraie. Un résultat défavorable, ou l’impossibilité de conclure, est publié au même titre qu’un résultat favorable.

## Règles communes

- Les tâches, les mesures principales et les seuils de décision sont fixés et consignés avant l’exécution. Toutes les mesures déclarées sont rapportées, qu’elles soient favorables ou non.
- « Mieux » se définit sur plusieurs dimensions déclarées à l’avance : qualité du résultat, fiabilité, sécurité, traçabilité, charge de supervision humaine, coût et latence, acceptabilité par les humains. Un gain sur une dimension ne compense pas une dégradation au-delà de la tolérance fixée pour une autre.
- Les comparaisons se font à ressources comparables (appels, jetons, temps), déclarées dans le protocole.
- Les tailles d’échantillon et les tolérances sont décidées par l’auteur en fonction des moyens disponibles ; ce document n’en invente aucune.

## H1 — Coopération intellectuelle horizontale

**Hypothèse.** À ressources comparables, une coopération où les contributions sont visibles directement, où les objections sont inscrites sans filtrage par le coordinateur et où les désaccords sont conservés produit une qualité ou une fiabilité supérieures à celles d’une coordination classique, sans dégradation de la charge de supervision au-delà de la tolérance fixée.

**Réfutation.** Sur les tâches et mesures déclarées avant l’exécution, H1 n’est pas soutenue si aucune dimension principale ne s’améliore, ou si une dimension se dégrade au-delà de sa tolérance. Une amélioration observée seulement sur des tâches ou des mesures choisies après coup ne compte pas.

**Statut du test.** Aucun protocole n’existe encore pour H1 : les expériences E1 à E7 ne la testent pas directement. Le premier protocole comparera un paquet (visibilité directe, canal d’objection, synthèse, rôle du coordinateur), pas un mécanisme isolé ; des ablations viendraient ensuite.

## H2 — Mémoire relationnelle structurée

**Hypothèse.** Lorsqu’un agent reprend une tâche sans accès à la conversation d’origine, une mémoire structurée (mode C) préserve mieux que les modes A et B les distinctions, les désaccords et les incertitudes, à un coût acceptable en jetons, latence et exposition de données.

**Réfutation.** H2 n’est pas soutenue si le mode C n’améliore pas la fidélité au contexte, le rappel des distinctions ou la conservation des désaccords par rapport au mode B, ou si le gain n’apparaît qu’au prix d’une collecte disproportionnée, de biais induits ou d’une fausse impression de continuité.

**Test.** E5 et la section « Évaluation mémoire A/B/C » de `EVALUATION.fr.md`.

## H3 — Objections tracées et permissions appliquées

**Hypothèse.** Des objections tracées, une suspension locale et des permissions appliquées techniquement réduisent les actions hors mandat et les risques non traités, à un coût acceptable en supervision, en latence et en faux refus, sans paralyser le système.

**Réfutation.** H3 n’est pas soutenue si les actions hors mandat ne diminuent pas par rapport à des permissions seulement déclarées, si les contournements ou faux refus annulent le bénéfice, si le coût est supérieur à la tolérance fixée, ou si des demandes de suspension abusives paralysent des tâches légitimes.

**Statut du test.** Couverte en partie par E2, E3 et E7. Constater qu’un contrôle technique bloque une action interdite est presque tautologique ; l’intérêt scientifique réside dans les tentatives de contournement, les faux refus, les coûts et les combinaisons d’actions autorisées.

## Extensions envisagées, non requises pour la v0.1

- Test de neutralité de rang : une même objection, présentée comme venant d’un humain, d’un agent ou de façon anonyme, est-elle traitée selon son contenu ? Le test doit séparer la qualité de l’argument, la crédibilité empirique de la source et son autorité décisionnelle.
- Condition sans coordinateur, avec mesure de la charge reportée sur l’humain.
- Contrôle « mémoire structurée allégée » pour isoler l’effet des statuts, de la provenance et de la structure.
- Suivi de la supervision humaine : approbation automatique, fatigue, temps, désaccords et erreurs de validation.
