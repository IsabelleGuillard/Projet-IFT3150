---
title: Travail réalisé
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Réalisation

> :bulb: Cette page sert à présenter les travaux réalisés incluant la conception.  
> Elle ne remplace pas le rapport final, mais permet de documenter progressivement les travaux réalisés, les décisions prises et les principaux résultats obtenus.


## Structure suggérée

> La structure suivante est donnée à titre indicatif.  
> Vous pouvez l’adapter selon la nature de votre projet.

---
### Architecture ou structure générale

> Présentez l’organisation générale du projet :
>
> - architecture logicielle ;
> - composants principaux ;
> - structure des données ;
> - technologies utilisées ;
> - environnement de développement ;
> - outils ou services externes.


#### Cas d'utilisation

##### Liste des cas d'utilisation

###### Tuteur
- CU01 — Créer un compte tuteur
- CU02 — Se connecter
- CU03 — Créer un profil élève
- CU04 — Modifier le profil élève
- CU05 — Modifier le profil tuteur
- CU06 — Prévisualiser des exercices
- CU07 — Assigner un devoir
- CU08 — Consulter la progression d'un élève

###### Élève
- CU09 — Accéder à la plateforme
- CU10 — Faire un devoir assigné
- CU11 — Pratiquer librement
- CU12 — Répondre à un exercice

##### Description des cas d'utilisation

###### Acteurs
- **Tuteur** : La personne qui accompagne les élèves et configure la plateforme pour l'élève
- **Élève** : L'élève du secondaire qui pratique les exercices
- **Système** : La plateforme MathPratique
- **LLM** : Le modèle de langue utilisé pour générer les exercices contextualisés et les explications


##### CU01 — Créer un compte tuteur

**Acteur principal** : Tuteur

**Scénario principal**
1. Le tuteur accède à la page d'accueil et sélectionne "Créer un compte tuteur".
2. Le tuteur saisit son nom, prénom, adresse courriel et mot de passe.
3. Le tuteur accepte les conditions d'utilisation.
4. Le système crée le compte et redirige le tuteur vers son tableau de bord.

**Scénarios alternatifs**
- 2a. L'adresse courriel est déjà associée à un compte existant.
  - 2a.1. Le système indique que l'adresse courriel est déjà utilisée.
  - 2a.2. Le système invite le tuteur à se connecter ou à réinitialiser son mot de passe.
  - 2a.3. Le scénario se termine.


##### CU02 — Se connecter

**Acteur principal** : Tuteur

**Scénario principal**
1. Le tuteur accède à la page de connexion.
2. Le tuteur saisit son adresse courriel et son mot de passe.
3. Le système vérifie les identifiants.
4. Le système redirige le tuteur vers son tableau de bord.

**Scénarios alternatifs**
- 3a. Les identifiants sont incorrects.
  - 3a.1. Le système indique que l'adresse courriel et/ou le mot de passe est incorrect.
  - 3a.2. Le scénario reprend à l'étape 2.


##### CU03 — Créer un profil élève

**Acteur principal** : Tuteur  
**Précondition** : Le tuteur est connecté.

**Scénario principal**
1. Le tuteur clique sur "Ajouter un élève".
2. Le système affiche un formulaire.
3. Le tuteur saisit le prénom, le nom, le niveau scolaire et les compétences
   à activer.
4. Le tuteur soumet le formulaire.
5. Le système vérifie que tous les champs obligatoires sont remplis.
6. Le système génère un code d'accès unique pour l'élève.
7. Le système sauvegarde le profil et redirige le tuteur vers la page
   de profil de l'élève.
8. Le tuteur peut ajouter des précisions supplémentaires (langue maternelle,
   centres d'intérêt, particularités d'apprentissage, notes libres, ratio
   d'exercices).

**Scénarios alternatifs**
- 5a. Le prénom, le nom ou le niveau scolaire n'est pas indiqué.
  - 5a.1. Le système indique les champs manquants.
  - 5a.2. Le scénario reprend à l'étape 3.
- 5b. Aucune compétence n'est activée.
  - 5b.1. Le système indique qu'au moins une compétence doit être activée.
  - 5b.2. Le scénario reprend à l'étape 3.


##### CU04 — Modifier le profil élève

**Acteur principal** : Tuteur  
**Précondition** : Le tuteur est connecté et l'élève existe dans son
tableau de bord.

**Scénario principal**
1. Le tuteur accède à la fiche de l'élève.
2. Le tuteur clique sur "Modifier".
3. Le système passe la fiche en mode édition.
4. Le tuteur modifie les informations souhaitées (compétences actives, profil LLM, etc).
5. Le tuteur clique sur "Enregistrer les modifications".
6. Le système sauvegarde les modifications.
7. Les nouveaux paramètres s'appliquent dès la prochaine session de l'élève.

**Scénarios alternatifs**
- 5a. Le tuteur clique sur "Annuler" avant d'enregistrer.
  - 5a.1. Le système annule les modifications et repasse en mode lecture.
  - 5a.2. Le scénario se termine.


##### CU05 — Modifier le profil tuteur

**Acteur principal** : Tuteur

**Précondition** : Le tuteur est connecté.

**Scénario principal**
1. Le tuteur accède à son profil.
2. Le tuteur modifie ses informations personnelles et ses préférences pédagogiques (approche, explications, ton, notes libres).
3. Le système sauvegarde les modifications.
4. Les nouvelles préférences s'appliquent dès la prochaine génération d'exercice ou d'explication.


##### CU06 — Prévisualiser des exercices

**Acteur principal** : Tuteur

**Précondition** : Le tuteur est connecté.

**Scénario principal**
1. Le tuteur accède à la section de prévisualisation.
2. Le tuteur sélectionne un élève (optionnel), une compétence, un niveau, un type d'exercice et un nombre d'exercices à générer.
3. Le tuteur lance la génération.
4. Le système affiche les exercices générés avec leur réponse attendue.
5. Si le tuteur n'est pas satisfait du résultat, il ajuste son profil ou le profil de l'élève et relance la génération.


##### CU07 — Assigner un devoir

**Acteur principal** : Tuteur
**Précondition** : Le tuteur est connecté et l'élève existe dans son
tableau de bord.

**Scénario principal**
1. Le tuteur accède à la fiche de l'élève et sélectionne "Créer un devoir".
2. Le tuteur configure une séquence d'exercices : pour chaque étape,
   il choisit une compétence, un niveau et un nombre d'exercices.
3. Le tuteur indique une date limite pour le devoir.
4. Le tuteur sauvegarde le devoir.
5. Le système associe le devoir à l'élève et le rend disponible dans
   son portail jusqu'à la date limite.

**Scénarios alternatifs**
- 2a. Le tuteur tente d'assigner une compétence non activée pour cet élève.
  - 2a.1. Le système indique que la compétence doit d'abord être activée
    dans le profil de l'élève.
  - 2a.2. Le scénario reprend à l'étape 2.


##### CU08 — Consulter la progression d'un élève

**Acteur principal** : Tuteur

**Précondition** : Le tuteur est connecté et l'élève a complété au moins un exercice.

**Scénario principal**
1. Le tuteur accède à la fiche de l'élève.
2. Le système affiche les statistiques globales (exercices complétés, taux de réussite, série active).
3. Le système affiche les niveaux atteints par compétence.
4. Le système affiche le temps de résolution moyen par type d'exercice.
5. Le système signale automatiquement les comportements suspects (temps de résolution anormalement court combiné à un taux de réussite élevé).


##### CU09 — Accéder à la plateforme (élève)

**Acteur principal** : Élève

**Scénario principal**
1. L'élève accède à la plateforme en saisissant son code d'accès sur la page d'accueil.
2. Le système vérifie la validité du code.
3. Le système charge le profil de l'élève et redirige vers l'écran de choix de concept.

**Scénarios alternatifs**
- 2a. Le code saisi est invalide.
  - 2a.1. Le système indique que le code n'est pas reconnu.
  - 2a.2. Le système invite l'élève à vérifier son code auprès de
    son tuteur.
  - 2a.3. Le scénario reprend à l'étape 1.


##### CU10 — Faire un devoir assigné

**Acteur principal** : Élève  
**Précondition** : Le tuteur a assigné un devoir à l'élève et la date
limite n'est pas dépassée.

**Scénario principal**
1. L'élève accède à la plateforme et voit le devoir assigné par son tuteur.
2. L'élève lance le devoir.
3. Le système génère le premier exercice selon les paramètres définis
   par le tuteur.
4. Appel du cas CU12 — Répondre à un exercice.
5. Le système passe à l'exercice suivant dans la séquence.
6. Les étapes 3 à 5 se répètent jusqu'à la fin de la séquence.
7. Le système affiche le résumé du devoir complété.

**Scénarios alternatifs**
- 1a. La date limite du devoir est dépassée.
  - 1a.1. Le système indique que le devoir n'est plus accessible.
  - 1a.2. Le système propose à l'élève de consulter ses devoirs
    précédents en lecture seule.
  - 1a.3. Le scénario se termine.


##### CU11 — Pratiquer librement

**Acteur principal** : Élève

**Précondition** : L'élève est connecté.

**Scénario principal**
1. L'élève choisit un concept parmi les compétences activées par son tuteur.
2. L'élève choisit de pratiquer une sous-compétence spécifique ou de réviser l'ensemble du module.
3. Le système génère un exercice adapté au niveau actuel de l'élève pour la compétence choisie.
4. Appel du cas CU12 — Répondre à un exercice.
5. Le système met à jour le niveau de l'élève selon l'algorithme adaptatif.
6. Les étapes 3 à 5 se répètent jusqu'à ce que l'élève choisisse d'arrêter.
7. Le système affiche le résumé de la session.


##### CU12 — Répondre à un exercice

**Acteur principal** : Élève

**Précondition** : Un exercice est affiché à l'écran.

**Scénario principal**
1. Le système affiche l'exercice (calculatoire ou contextualisé) et démarre le chronomètre.
2. L'élève saisit sa réponse et soumet.
3. Le système arrête le chronomètre et vérifie la réponse.
4. La réponse est correcte : le système affiche un feedback positif et enregistre le résultat.

**Scénarios alternatifs**
- 4a. La réponse est incorrecte.
  - 4a.1. Le système affiche la bonne réponse.
  - 4a.2. Le système transmet au LLM l'énoncé, la réponse de l'élève, la bonne réponse ainsi que les profils tuteur et élève.
  - 4a.3. Le LLM génère une explication personnalisée.
  - 4a.4. Le système affiche l'explication à l'élève.
  - 4a.5. Le scénario se termine.
- 2a. L'élève indique qu'il ne sait pas.
  - 2a.1. Le système affiche la bonne réponse et l'explication.
  - 2a.2. Le scénario se termine.

---
#### Niveaux de difficulté par compétence

Les exercices calculatoires sont organisés en niveaux de difficulté pour chaque compétence.

##### Simplification de fractions — 4 niveaux

La difficulté progresse selon la complexité du PGCD à identifier.

- **Niveau 1** : Le PGCD est toujours 2. Le numérateur et le dénominateur sont des nombres pairs entre 2 et 24.
  Exemple : 6/10 devient 3/5.
- **Niveau 2** : Le PGCD est un nombre premier parmi 3, 5 ou 7. Les valeurs vont jusqu'à 49.
  Exemple : 15/25 devient 3/5.
- **Niveau 3** : Le PGCD est un entier entre 2 et 12, incluant les nombres composés (4, 6, 8, 9, 10, 12). Les valeurs vont jusqu'à 144. L'élève   ne peut plus deviner le PGCD visuellement et doit le calculer.
  Exemple : 48/72 devient 2/3.
- **Niveau 4** : Le PGCD est un entier entre 6 et 15, avec de grands numérateurs et dénominateurs allant jusqu'à 144.
  Exemple : 84/126 devient 2/3.

Dans tous les cas, le numérateur est différent du dénominateur.


##### Addition et soustraction de fractions — 4 niveaux

La difficulté progresse selon la complexité du dénominateur commun à trouver. L'opérateur (+ ou −) est choisi aléatoirement à chaque exercice. Pour la soustraction, le résultat est toujours positif.

- **Niveau 1** : Les deux fractions ont le même dénominateur, entre 2 et 50. L'élève additionne ou soustrait directement les numérateurs.
  Exemple : 1/5 + 2/5 = 3/5.
- **Niveau 2** : Les dénominateurs sont différents, mais l'un est un multiple direct (2, 3, 5) de l'autre. L'élève ne doit convertir qu'une       seule fraction.
  Exemple : 1/2 + 1/4 = 3/4.
- **Niveau 3** : Les dénominateurs sont différents avec un PPCM simple (2, 3, 4, 5, 6). Les valeurs vont jusqu'à 72. L'élève doit convertir les   deux fractions.
  Exemple : 1/3 + 1/4 = 7/12.
- **Niveau 4** : Les dénominateurs sont différents avec un PPCM moins évident (valeurs plus grandes comme 6, 7, 8, 9, 10, 12). Le calcul du       PPCM est non trivial.
  Exemple : 5/6 + 3/8 = 29/24.


##### Multiplication de fractions — 3 niveaux

La difficulté progresse selon la taille des nombres et la nécessité de simplifier le résultat. La seule opération requise est la multiplication des numérateurs entre eux et des dénominateurs entre eux.

- **Niveau 1** : Numérateurs et dénominateurs entre 1 et 9. Le résultat est irréductible : aucune simplification n'est nécessaire.
  Exemple : 2/3 × 1/5 = 2/15.
- **Niveau 2** : Numérateurs et dénominateurs entre 1 et 9. Le résultat doit être simplifié après la multiplication.
  Exemple : 2/3 × 3/4 = 6/12 devient 1/2.
- **Niveau 3** : Numérateurs et dénominateurs entre 1 et 15. Le résultat doit être simplifié, avec des nombres plus grands rendant la             simplification moins évidente.
  Exemple : 4/5 × 5/8 = 20/40 devient 1/2.


##### Division de fractions — 3 niveaux

La difficulté progresse de la même façon que pour la multiplication. La méthode est d'inverser la deuxième fraction et de multiplier.

- **Niveau 1** : Numérateurs et dénominateurs entre 1 et 9. Le résultat est irréductible après inversion et multiplication.
  Exemple : 2/3 ÷ 1/5 = 2/3 × 5/1 = 10/3.
- **Niveau 2** : Numérateurs et dénominateurs entre 1 et 9. Le résultat doit être simplifié.
  Exemple : 2/3 ÷ 4/9 = 2/3 × 9/4 = 18/12 devient 3/2.
- **Niveau 3** : Numérateurs et dénominateurs entre 1 et 15. Le résultat doit être simplifié, avec des nombres plus grands.
  Exemple : 4/5 ÷ 8/15 = 4/5 × 15/8 = 60/40 devient 3/2.
---

##### Fonctionnalités ou composantes réalisées

> Présentez les principales fonctionnalités, modules ou composantes développés.
>
> Vous pouvez inclure :
>
> - captures d’écran ;
> - diagrammes ;
> - démonstrations ;
> - extraits de code ;
> - prototypes.

##### Difficultés rencontrées

> Décrivez les principaux défis rencontrés durant le projet :
>
> - techniques ;
> - méthodologiques ;
> - organisationnels ;
> - liés aux outils ou technologies.

##### Décisions et ajustements

> Présentez les changements importants effectués durant le trimestre :
>
> - changement d’approche ;
> - ajustement des objectifs ;
> - nouvelles contraintes ;
> - simplifications ;
> - améliorations apportées.
