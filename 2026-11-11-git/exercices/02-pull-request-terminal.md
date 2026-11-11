# Exercice 2 · La même chose, en ligne de commande

**À la maison · 15 min · Git installé**

Le but : refaire l'exercice 1 avec les commandes, et voir les quatre boîtes du modèle mental de tes propres yeux.

## Une fois : se connecter à GitHub

GitHub n'accepte plus les mots de passe dans le terminal. Le plus simple : installer [GitHub CLI](https://cli.github.com), puis

```bash
gh auth login        # choisis GitHub.com, HTTPS, et connecte-toi dans le navigateur
```

## L'exercice

- [ ] **Clone ton fork** (celui de l'exercice 1) :
  ```bash
  git clone https://github.com/<ton-compte>/mercredis-numeriques.git
  cd mercredis-numeriques
  ```
- [ ] **Crée une branche :**
  ```bash
  git switch -c complete-ma-fiche
  ```
- [ ] **Modifie** `participants/<prenom>.md` : ajoute une ligne, par exemple `- **Mon outil préféré** : …`
- [ ] **Regarde les boîtes.** Lance `git status` après chaque étape et observe ce qui change :
  ```bash
  git status                       # fichier modifié, pas encore dans l'index
  git diff                         # ce qui a changé
  git add participants/<prenom>.md
  git status                       # maintenant dans l'index
  git commit -m "Ajoute mon outil préféré à ma fiche"
  git status                       # propre ; le commit est dans l'historique
  git log --oneline                # le voilà
  ```
- [ ] **Push :**
  ```bash
  git push -u origin complete-ma-fiche
  ```
- [ ] **Ouvre la pull request,** soit sur la page de ton fork, soit avec `gh pr create`.

**Bonus.** `git log --oneline --graph --all` dessine l'historique avec les branches.
