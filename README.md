# Exercice Git & GitHub — projet d'équipe

Ce petit dépôt sert à pratiquer `clone`, `status`, `add`, `commit`, `push`, `pull`, puis la résolution d'un conflit. Travaillez en binôme sur **un dépôt GitHub par binôme**.

## 1. Premier partage

1. La personne A clone le dépôt et ouvre le dossier dans un terminal.
2. A ajoute son prénom sur une nouvelle ligne dans `equipe.md`.
3. A exécute `git status`, `git diff`, `git add equipe.md`, puis `git commit -m "Ajoute mon prénom"` et `git push`.
4. La personne B clone le dépôt (ou fait `git pull` si elle l'avait déjà cloné) et vérifie que le prénom de A apparaît.
5. B ajoute son prénom sur une autre ligne, crée un commit et pousse. A fait `git pull`.

## 2. Conflit volontaire

Avant de commencer, **A et B doivent tous les deux avoir la même version** de `accueil.md`. Dans chaque copie locale du dépôt, exécuter :

```sh
git config pull.rebase false
git pull
```

Ensuite, sans faire de nouveau `pull` entre les étapes :

1. A remplace la phrase sous « Message du groupe » dans `accueil.md` par sa propre phrase. A crée un commit et pousse.
2. B remplace **cette même phrase** par une phrase différente dans sa copie locale. B crée un commit, puis tente `git push` : Git refuse car le dépôt distant a avancé.
3. B exécute `git pull`. Git signale un conflit dans `accueil.md`.
4. B ouvre le fichier, choisit le texte final avec A et supprime les lignes `<<<<<<<`, `=======` et `>>>>>>>`.
5. B exécute `git status`, `git add accueil.md`, `git commit`, puis `git push`.
6. A fait `git pull` et vérifie la phrase finale.

Si `git status` indique un *rebase* en cours, utiliser `git rebase --continue` après `git add` au lieu de `git commit`. N'utilisez pas `git push --force` pour cet exercice.

## 3. Bonus : branche et pull request

1. Mettre `main` à jour avec `git pull`.
2. Créer une branche : `git switch -c ajout-contact`.
3. Créer un fichier `contact.md` avec le prénom des membres du binôme.
4. Créer un commit et publier la branche : `git push -u origin ajout-contact`.
5. Sur GitHub, ouvrir une pull request vers `main`. L'autre personne relit, puis fusionne.
6. Revenir sur `main` avec `git switch main`, puis `git pull`.

En cas de doute, commencer par `git status` et lire son message avant de lancer une autre commande.
