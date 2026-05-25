---
title: Vue d'ensemble du projet
---

# Vue d'ensemble du projet
 
**Session:** Été 2026  
**Auteure:** Isabelle Guillard (20278907)   
**Thème(s):** Algorithmique, LLM, systèmes adaptatifs, développement web   
**Superviseur:** Louis Edouard Lafontant  
    
## Description du projet

### Contexte

L'enseignement des mathématiques au secondaire repose en grande partie sur la pratique d'exercices de façon répétée, ce qui permet aux élèves de consolider les concepts et de maîtriser les différentes méthodes de résolution de problèmes. Dans un contexte de tutorat individuel ou de soutien scolaire, cette pratique se fait lors des séances, mais il peut arriver de donner des exercices à pratiquer en dehors des séances sans qu'il y ait nécessairement un suivi structuré ou d'adaptation au niveau réel de l'élève.

Les plateformes éducatives existantes (Khan Academy, Alloprof, etc.) offrent des ressources générales, mais ne permettent pas à un tuteur de cibler précisément les concepts travaillés avec un élève donné, ni de suivre sa progression de façon précise. Ce sont généralement des plateformes que l'élève doit naviguer seul et dont les exercices sont génériques et prédéterminés. La plateforme Alloprof est une plateforme éducative fortement utilisée pour les explications qu'elle offre.

### Problématique

Les élèves du secondaire qui bénéficient d'un suivi en tutorat privé manquent d'un outil de pratique autonome qui s'adapte à leur niveau réel et qui permet à leur tuteur de cibler les concepts à travailler et de suivre leur progression entre les séances. Les plateformes existantes comme Khan Academy ou Alloprof sont conçues pour une utilisation autonome et généralisée. Elles ne permettent pas à un tuteur de configurer l'environnement de pratique d'un élève spécifique, ni d'observer les difficultés de cet élève.

Il y a donc une discontinuité entre le travail effectué en séance et la pratique autonome de l'élève, ce qui limite l'efficacité de l'accompagnement. De plus, les exercices proposés par ces plateformes sont prédéterminés et ne s'adaptent pas dynamiquement aux erreurs récentes de l'élève sur une compétence donnée. Par exemple, un élève qui maîtrise bien l'addition de fractions à dénominateurs égaux mais qui bloque sur la simplification continuera à recevoir des exercices génériques plutôt que des exercices ciblant précisément sa difficulté.

### Proposition et objectifs

Ce projet propose le développement d'une plateforme web de pratique en mathématiques destinée aux élèves du secondaire, conçue pour s'intégrer naturellement dans un contexte de tutorat. La plateforme comprendrait deux portails distincts : un portail tuteur permettant de gérer les profils d'élèves et de suivre leur progression, et un portail élève offrant un accès simplifié par code unique à des exercices générés algorithmiquement et adaptés dynamiquement au niveau de l'élève.

### Méthodologie

Le projet suit une démarche de développement itératif organisée en quatre phases principales.

La première phase (semaines 1 et 2) est consacrée à l'analyse des exigences : définition
de la portée, validation des besoins auprès de tuteurs du milieu et documentation des
études préliminaires.

La deuxième phase (semaines 3 et 4) couvre l'exploration technique et la prise de décisions
architecturales : expérimentation avec le LLM retenu, définition des principales composantes
du système et de leurs interactions, conception des maquettes de l'interface et finalisation
de l'architecture.

La troisième phase (semaines 5 à 8) constitue le développement principal : implémentation
du moteur de génération algorithmique d'exercices par compétence, de l'algorithme adaptatif,
de l'interface élève, du portail tuteur et de l'intégration LLM pour la génération
d'exercices contextualisés et les explications personnalisées après erreur.

La quatrième phase (semaines 9 à 12) est dédiée aux tests, aux ajustements, à la rédaction
du rapport final et à la préparation de la présentation.

### Validation et Évaluation

La validation du projet s'effectue à deux niveaux.

**Validation technique**

Pour les exercices calculatoires, la validation repose sur des tests automatisés vérifiant
que les exercices produits sont mathématiquement corrects et conformes aux contraintes du
niveau ciblé, et que la vérification des réponses fonctionne correctement pour tous les
formats de saisie acceptés. L'algorithme adaptatif est validé par simulation de profils
d'élèves types (progression rapide, progression lente, régression) et vérification que
les niveaux évoluent conformément aux seuils définis.

Pour les exercices contextualisés générés par le LLM, la validation est effectuée
manuellement : un échantillon d'exercices générés est examiné pour s'assurer que l'énoncé
correspond bien aux paramètres numériques fournis, qu'aucune ambiguïté n'est introduite
dans la réponse attendue, et que le contexte est approprié pour des élèves du secondaire.

**Validation pratique**

La plateforme sera soumise à des sessions de test avec les tuteurs ayant exprimé leur
intérêt lors des entretiens préliminaires. Les indicateurs retenus incluent la capacité
à compléter une session sans assistance, la lisibilité des exercices générés, la pertinence
perçue du niveau de difficulté et la qualité des explications fournies par le LLM après
erreur. Les retours seront documentés et les ajustements apportés seront consignés dans
le rapport final.

## Échéancier

    Le suivi complet est disponible dans la page [Suivi de projet].

| Activités                        | Début  | Fin     | Livrable                              | Statut      |
|----------------------------------|--------|---------|---------------------------------------|-------------|
| Ouverture de projet              | 7 mai  | 7 mai   | Déploiement du site de documentation  | ✅ Terminé  |
| Études préliminaires             | 7 mai  | 18 mai  | Document d'analyse                    | ✅ Terminé  |
| Analyse des exigences            | 19 mai | 24 mai  | Diagrammes d'architecture maquettes   | ✅ Terminé  |
| Exploration LLM et architecture  | 24 mai | 1 juin  | Décisions architecturales documentées | 🔄 En cours |
