---
title: Suivi du projet
---
# Suivi de projet

---

## Semaines 1 et 2 (5-19 mai 2026)

### Objectifs de la période

- Clarifier la problématique et le contexte du projet
- Explorer et comparer les solutions existantes
- Définir la portée et les fonctionnalités de l'application
- Valider les besoins auprès de tuteurs du milieu
- Prendre les premières décisions de conception

### Travail réalisé

!!! abstract "Avancement"
    - [x] Analyse comparative de trois plateformes existantes
        - Alloprof, Khan Academy et Netmath évaluées selon plusieurs critères, dont les fonctionnalités offertes, l'adaptation au niveau de               l'élève, la personnalisation par le tuteur et l'interface utilisateur
    - [x] Validation auprès de tuteurs
        - Deux appels téléphoniques avec des tuteurs en mathématiques au secondaire (11 et 15 mai 2026)
        - Les fractions et l'algèbre ressortent comme concepts difficiles chez les deux tuteurs, confirmant le choix de concepts de départ
        - L'intégration d'un LLM pour les explications est identifiée comme une fonctionnalité utile par un des tuteurs
    - [x] Définition du fonctionnement global de l'application
        - Deux portails distincts : portail tuteur et portail élève
        - Accès élève par un code unique sans création de compte
        - Quatre compétences ciblées pour le module sur les fractions :
          simplification, addition et soustraction, multiplication et division
        - Niveaux de difficulté définis pour chaque compétence
    - [x] Études préliminaires
        - Compréhension du problème, analyse des solutions existantes, contraintes et besoins

### Décisions et ajustements

!!! info "Décisions"
    - Génération algorithmique des exercices avec gabarits contextuels
        - La génération par LLM des énoncés a été écartée en raison du problème de vérification de la bonne réponse. Le LLM est réservé aux               explications personnalisées après erreur
    - Exercices de deux types : calculatoires et contextualisés
        - Les exercices contextualisés utilisent des gabarits de situations réelles dans lesquels les paramètres numériques sont insérés
          algorithmiquement
    - Nombres fractionnaires traités comme niveau bonus optionnel
        - Isolés des niveaux principaux pour chaque compétence concernée, activables par le tuteur selon le profil de l'élève
    - Mini-chat LLM limité au contexte de l'exercice en cours
        - Un chat libre non contrôlé a été écarté au profit de boutons prédéfinis complétés par un mini-chat réinitialisé à chaque
          nouvel exercice
    - Suivi du temps de résolution inclus dans le portail tuteur
        - Permet de détecter les comportements suspects en corrélant le temps de réponse avec le taux de réussite

### Difficultés rencontrées

!!! warning "Difficultés"
    - Décision sur l'approche de génération d'exercices contextualisés
        - La génération libre par LLM semblait attrayante mais introduit un problème de vérification des réponses.
