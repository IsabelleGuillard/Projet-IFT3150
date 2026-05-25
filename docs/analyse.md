---
title: Études préliminaires
---
# Études préliminaires

## Compréhension du problème

Les élèves du secondaire qui bénéficient d'un suivi en tutorat privé manquent d'un outil de pratique autonome qui s'adapte à leur niveau réel et qui permet à leur tuteur de cibler les concepts à travailler et de suivre leur progression entre les séances. Les plateformes existantes comme Khan Academy ou Alloprof sont conçues pour une utilisation autonome et généralisée. Elles ne permettent pas à un tuteur de configurer l'environnement de pratique d'un élève spécifique, ni d'observer les difficultés de cet élève.

Il y a donc une discontinuité entre le travail effectué en séance et la pratique autonome de l'élève, ce qui limite l'efficacité de l'accompagnement. De plus, les exercices proposés par ces plateformes sont prédéterminés et ne s'adaptent pas dynamiquement aux erreurs récentes de l'élève sur une compétence donnée. Par exemple, un élève qui maîtrise bien l'addition de fractions à dénominateurs égaux mais qui bloque sur la simplification continuera à recevoir des exercices génériques plutôt que des exercices ciblant précisément sa difficulté.

De plus, les tuteurs qui donnent des devoirs à faire entre les séances doivent les corriger dans leur temps libre ou lors des séances. Les tuteurs bénéficieraient donc d'une plateforme qui ferait ce travail à leur place tout en leur permettant d'avoir accès à ce que chaque élève aura pratiqué entre les séances.

---

## Analyse des solutions ou approches existantes

Trois plateformes ont été analysées en détail : Alloprof, Khan Academy et Netmath. Ces plateformes ont été sélectionnées pour leur pertinence dans le contexte québécois francophone au niveau secondaire.

### Alloprof

Alloprof s'impose comme la référence incontournable pour les explications de contenu dans le système scolaire québécois. Ses fiches pédagogiques, rédigées en français et alignées avec le programme d'éducation québécoise, sont d'une qualité reconnue.

Par contre, son module d'exercices accuse un retard significatif : l'interface est vieillissante, l'élève doit lui-même choisir son niveau de difficulté et le nombre de questions, et le retour après une mauvaise réponse se limite à afficher la bonne réponse en rouge, sans explication. Il n'existe aucun mécanisme d'adaptation au niveau de l'élève, et aucune possibilité pour un tuteur de configurer ou de suivre la pratique d'un élève en particulier. De plus, l'interface ne permet pas de saisir les réponses en notation mathématique standard, forçant l'élève à écrire les fractions sous forme de texte plutôt que sous leur forme visuelle habituelle. La plateforme d'exercices offre une expérience peu stimulante pour l'élève, sans mécanisme de valorisation de la progression ni de transition naturelle entre les exercices.

**Forces :** contenu pédagogique de qualité, aligné avec le programme québécois, entièrement gratuit.

**Limites :** interface d'exercices désuète, aucune adaptation dynamique, saisie des réponses en texte brut uniquement , retour après erreur insuffisant, expérience d'exercices peu engageante.

### Khan Academy

Khan Academy offre une interface d'exercices bien conçue avec des retours
visuels et sonores engageants. Son système d'indices progressifs, qui peut
guider l'élève jusqu'à la solution étape par étape, constitue une approche
pédagogique intéressante. Par contre, elle peut être problématique lorsque
plusieurs méthodes de résolution existent, ou lorsque l'élève exploite
les indices pour obtenir directement la réponse sans réelle compréhension.

La plateforme souffre d'un obstacle majeur pour le marché québécois : elle est en anglais par défaut, et le changement de langue nécessite la création d'un compte. Son interface, chargée en informations, peut également être déstabilisante pour des élèves du secondaire. Comme Alloprof, elle est conçue pour un usage autonome et généraliste. Je n'ai pas testé le portail tuteur, mais de ce que j'ai compris, c'est la même interface et les mêmes exercices. Le seul changement est que le tuteur peut observer la progression de l'élève.

**Forces :** interface engageante, indices progressifs, résumé de fin de session, gratuit.

**Limites :** anglais par défaut, non aligné sur le programme québécois, interface chargée, indices pouvant donner directement la réponse, compte requis pour sauvegarder les progrès.

### Netmath

Netmath est la plateforme qui se rapproche le plus des besoins identifiés. Entièrement conçue au Québec et alignée sur le programme ministériel, elle propose une interface particulièrement adaptée aux jeunes, avec des exercices interactifs, un clavier virtuel mathématique, une lecture audio des questions favorisant l'accessibilité, et un lexique mathématique intégré.

Sa gestion des erreurs est pédagogiquement réfléchie : après consultation du solutionnaire, un exercice légèrement différent est généré pour éviter la simple copie de la réponse. Même après une bonne réponse, l'élève peut consulter une explication, reconnaissant ainsi qu'une réponse correcte n'implique pas nécessairement une compréhension solide.

Malgré ces qualités, Netmath présente des limites importantes dans un contexte de tutorat. Ses exercices sont prédéfinis et suivent des gabarits fixes, sans adaptation dynamique au niveau de l'élève. La personnalisation par l'enseignant se limite à l'envoi d'exercices ciblés, sans suivi de la progression par compétence. Par ailleurs, la fin d'une session d'exercices est peu valorisante pour l'élève, sans message de félicitations ni navigation claire vers la suite.

**Forces :** aligné avec le programme québécois, interface moderne et adaptée aux jeunes, accessibilité audio, lexique intégré, gestion pédagogique des erreurs, option enseignant disponible.

**Limites :** exercices prédéfinis, aucune adaptation dynamique par compétence, personnalisation par le tuteur limitée, expérience de fin de session décevante, payant pour les fonctionnalités enseignant.

### Tableau comparatif

|                                  | Alloprof          | Khan Academy          | Netmath                 | Mon outil           |
|----------------------------------|-------------------|-----------------------|-------------------------|---------------------|
| Langue                           | Français (Québec) | Anglais par défaut    | Français (Québec)       | Français (Québec)   |
| Alignement programme québécois   | ✅                | ❌                     | ✅                      | ✅                  |
| Interface adaptée aux jeunes     | ❌                | ✅                     | ✅                      | ✅                  |
| Exercices adaptatifs             | ❌                | ⚠️ Partiel             | ❌                      | ✅ Par compétence   |
| Explication après erreur         | ❌                | ⚠️ Indices progressifs | ⚠️ Solutionnaire        | ✅ LLM personnalisé |
| Personnalisation par le tuteur   | ❌                | ⚠️ Limitée             | ⚠️ Limitée              | ✅                  |
| Accès sans compte (élève)        | ❌                | ❌                     | ⚠️                      | ⚠️ Code unique      |
| Suivi de progression             | ❌                | ⚠️ Compte requis       | ⚠️ Enseignant seulement | ✅ Par compétence   |
| Accessibilité                    | ❌                | ⚠️                     | ✅ Audio, lexique       | ⚠️ À voir           |
| Contexte cible                   | Autonome          | Autonome              | Classe ou autonome      | Tutorat privé       |
| Coût                             | Gratuit           | Gratuit               | Payant (école)          | À déterminer        |

---

## Contraintes et besoins

### Contraintes techniques

- Frontend : React
- Rendu mathématique : À déterminer
- Backend : Python
- Base de données : Supabase
- LLM : À déterminer

### Contraintes humaines

Le projet est développé individuellement en environ 10 semaines. L'apprentissage des différentes technologies doit être réalisé en cours de projet.

### Contraintes temporelles

La session d'été 2026 s'étend sur 12 semaines, de mai à août. L'objectif est d'avoir une application fonctionnelle et testée avant la présentation finale au début août.

### Besoins identifiés

Les besoins principaux ont été identifiés à partir de l'analyse des solutions existantes et des entretiens avec deux tuteurs en plus de mon expérience personnelle. Ils comprennent une génération algorithmique d'exercices par compétence et par niveau avec suffisamment de variété pour éviter les répétitions, un algorithme adaptatif opérant indépendamment sur chaque compétence (simplification, addition et soustraction, multiplication, division), une interface élève simple accessible via code unique sans création de compte, un portail tuteur permettant de gérer les profils, d'activer les concepts et de suivre la progression, ainsi qu'un suivi du temps de résolution pour détecter les comportements suspects.

---


## Explorations techniques ou conceptuelles

### Validation auprès des tuteurs

Afin de recruter des participants, une publication a été publiée dans un groupe Facebook de tuteurs montréalais comptant près de 6000 membres, invitant les tuteurs et enseignants en mathématiques au secondaire à partager leur expérience dans le cadre du développement d'une plateforme web de pratique en mathématiques pour le secondaire. Deux tuteurs ont répondu favorablement et des entretiens informels ont été conduits avec chacun d'eux afin de valider les besoins avant le développement. Les entretiens ont été réalisés sous forme d'appels téléphoniques en mai 2026.

#### Tuteur #1 — 11 mai 2026
*Profil : tuteur en mathématiques et sciences au secondaire et
au cégep.*

Ce tuteur donne des devoirs uniquement lorsqu'il identifie des lacunes spécifiques chez un élève. Lorsqu'il en donne, la correction se fait soit sur son temps personnel, soit en consacrant une dizaine de minutes au début de la séance suivante, ce qui représente une charge non négligeable dans son suivi.

Les concepts qu'il identifie comme les plus difficiles pour ses élèves sont le développement d'expressions algébriques, les fractions et les nombres irrationnels (racines carrées).

Concernant la plateforme, il souligne que l'intégration d'un système d'explication par intelligence artificielle serait déterminante pour que l'outil soit réellement profitable. Selon lui, la possibilité d'ouvrir une conversation entre l'élève et l'IA lorsque celui-ci est bloqué est une condition essentielle à l'utilité de la plateforme. Avec cette fonctionnalité, il considère que l'outil serait utile dans sa pratique de tutorat.

#### Tutrice #2 — 15 mai 2026
*Profil : tutrice multidisciplinaire au secondaire, majoritairement en français, mathématiques et sciences.*

Cette tutrice utilise occasionnellement des outils comme Kahoot pour rendre les séances plus engageantes avec ses élèves. Les
concepts qu'elle identifie comme les plus problématiques sont les conversions d'unités, les fractions, ainsi que l'algèbre, notamment les manipulations algébriques et la résolution d'équations.

Elle n'a pas formulé de commentaire critique sur la plateforme proposée, mais a exprimé un intérêt marqué : elle serait très intéressée à utiliser un tel outil dès qu'il serait disponible.

#### Observations générales

Ces deux entretiens permettent de dégager plusieurs éléments pertinents pour la conception du projet. Les fractions ressortent
comme concept difficile chez les deux tuteurs, ce qui confirme la pertinence du choix de ce module comme point de départ du développement. La charge liée à la correction des travaux hors séance est un irritant réel, que la plateforme adresse directement en offrant une vérification automatique et un suivi de progression accessible à tout moment. Enfin, la demande explicite d'un système d'explication par IA de la part du Tuteur #1 valide la décision d'intégrer un LLM pour les explications personnalisées après erreur.

### Explorations techniques

*À compléter*

> Présentez les premiers tests, prototypes, validations ou explorations réalisés :
>
> - technologies testées ;
> - essais d’architecture ;
> - expériences ;
> - validation d’idées ;
> - maquettes ou esquisses.

---

## Choix retenus


### Génération d'exercices — approche hybride algorithmique et LLM

Deux types d'exercices sont générés selon des approches distinctes.

Les exercices calculatoires sont générés de façon entièrement algorithmique : les paramètres numériques sont produits selon les contraintes du niveau ciblé, ce qui garantit que la bonne réponse est connue à l'avance et vérifiable de manière déterministe.

Les exercices contextualisés sont générés par un LLM à partir des paramètres numériques produits algorithmiquement. Le LLM reçoit les valeurs numériques et les paramètres de l'opération, et génère un énoncé ancré dans une situation réelle. Un encadrement rigoureux du prompt assure que la bonne réponse reste vérifiable. Le LLM est également utilisé pour générer des explications personnalisées après erreur et pour alimenter le mini-chat d'assistance.

### Accès élève — code unique sans compte

La création de comptes pour les élèves a été écartée en raison de la complexité légale associée aux mineurs (Loi 25 au Québec). Un code unique généré par le tuteur permet à l'élève d'accéder à son profil sans inscription, tout en maintenant la persistance des données.

### Portail tuteur

Le portail tuteur est inclus dans l'outil, car il est central au modèle d'affaires envisagé, soit le tuteur payant et les élèves accédant gratuitement, et nécessaire pour démontrer la proposition de valeur complète lors de la présentation finale.

---

## Références

### Articles scientifiques

Awang, L. A., Yusop, F. D., & Danaee, M. (2025). Current practices and future direction of artificial intelligence in mathematics education: A systematic review. *International Electronic Journal of Mathematics Education*, 20(2), em0823. https://doi.org/10.29333/iejme/16006

### Plateformes analysées

Alloprof. (s.d.). *Alloprof*. https://www.alloprof.qc.ca

Khan Academy. (s.d.). *Khan Academy*. https://www.khanacademy.org

Netmath. (s.d.). *Netmath*. https://netmath.ca

### Documentation technique

*À compléter*
