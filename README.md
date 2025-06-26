# Projet de Gestion de Version avec Git

Ce projet a été réalisé pour mettre en pratique les bonnes pratiques de gestion de version avec Git, en suivant une stratégie de branches de type "Git Flow" simplifiée.

## Stratégie de branchement

* `main` : **Branche finale stable.** Contient le code propre et validé, prêt pour la mise en ligne.
* `dev` : **Branche d'intégration.** Elle sert à regrouper et valider toutes les fonctionnalités développées avant la publication. C'est notre environnement "semi-stable".
* `feature/*` : **Branches de développement par fonctionnalité.** Chaque nouvelle fonctionnalité (structure HTML, thème CSS, interactions JS) a été développée sur sa propre branche, par exemple `feature/css-theme`.
* `test/*` : **Branches de tests intermédiaires.** Elles ont été utilisées pour tester et valider le code d'une fonctionnalité avant son intégration sur la branche `dev`.

## Flux de travail et étapes suivies

Le développement a suivi le flux de travail recommandé : `feature/*` -> `test/*` -> `dev` -> `main`.

1.  **Initialisation du projet** : Création de la structure de fichiers et initialisation du dépôt Git avec `git init`.
2.  **Mise en place de la structure de branches** : Création des branches `main` et `dev` à partir du commit initial.
3.  **Développement par fonctionnalité** : Pour chaque tâche (HTML, CSS, JS), une branche `feature/*` a été créée à partir de `dev`. Le code a été développé et committé sur cette branche.
4.  **Tests intermédiaires** : Chaque branche `feature/*` a été fusionnée dans la branche `test/frontend` pour réaliser les tests.
5.  **Intégration** : Une fois les tests réussis, le code de `test/frontend` a été fusionné dans la branche `dev`.
6.  **Validation finale** : Une fois toutes les fonctionnalités intégrées et validées sur `dev`, la branche `dev` a été fusionnée dans la branche `main` pour la version finale du projet.
7.  **Publication** : Le dépôt local a été poussé sur GitHub pour la publication et le partage.

## Commandes Git utilisées

Voici une liste des commandes Git essentielles utilisées pour ce projet :

* `git init` : Pour initialiser le dépôt.
* `git add .` : Pour ajouter les fichiers à la zone de staging.
* `git commit -m "..."` : Pour enregistrer les modifications avec un message clair.
* `git branch <nom>` : Pour créer de nouvelles branches.
* `git checkout <nom>` / `git switch <nom>` : Pour basculer entre les branches.
* `git merge <branche>` : Pour fusionner une branche dans la branche actuelle.
* `git status` : Pour vérifier l'état du dépôt.
* `git log --oneline --graph --all` : Pour visualiser l'historique des commits et des fusions.
* `git push origin <branche>` : Pour envoyer les commits sur le dépôt distant.