# Préparation de la séance

Ce dossier est le dépôt initial à publier sur GitHub. Garder `accueil.md` tel quel jusqu'au début de l'exercice : les deux étudiants doivent partir de la même phrase pour produire un conflit.

## Avant le cours

1. Publier ce dépôt sur GitHub, avec `main` comme branche par défaut.
2. Donner l'accès en écriture aux étudiants qui feront les exercices.
3. Prévoir **un dépôt par binôme** pour que les manipulations des groupes ne se gênent pas. Le dépôt publié peut servir de modèle GitHub ; chaque binôme crée sa copie à partir du modèle.
4. Faire vérifier `git --version` et l'authentification GitHub sur les postes.

## Animation

- Premier partage : A pousse son prénom ; B récupère, ajoute le sien et pousse ; A récupère.
- Conflit : s'assurer que les deux copies sont synchronisées avant les modifications, puis faire travailler A et B sans `pull` intermédiaire. Le second `push` est refusé, et son `pull` déclenche le conflit.
- Demander aux étudiants de lire `git status` à chaque étape. Pour obtenir une fusion simple dans cet exercice, exécuter `git config pull.rebase false` dans chaque copie locale.
- Bonus : utiliser la branche `ajout-contact` et la pull request décrites dans `README.md` si le temps le permet.

Les étudiants peuvent laisser `ENSEIGNANT.md` de côté ; les consignes à suivre sont dans `README.md`.
