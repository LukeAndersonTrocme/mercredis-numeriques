# Exercice 3 · Ton vrai projet

**À la maison · 15 min · Git et GitHub CLI installés (cf. exercice 2)**

C'est l'exercice qui compte. Les autres étaient de l'entraînement ; celui-ci change tes habitudes.

Prends ton projet de recherche actif. Celui organisé (ou pas encore) selon la [session du 14 octobre](https://popgen.ca/lukezone/organisation-scripts-fichiers).

- [ ] **Initialise le dépôt :**
  ```bash
  cd ~/chemin/vers/mon-projet
  git init
  ```
- [ ] **Écris le `.gitignore` AVANT le premier commit.** C'est l'étape la plus importante : une fois des données commitées, elles restent dans l'historique même si tu les supprimes ensuite.
  ```
  data/
  output/
  *.Rhistory
  .Rproj.user/
  .DS_Store
  ```
  Adapte selon ton projet. Gros fichiers, données de participants, mots de passe, clés d'API : rien de tout ça ne va dans Git.
- [ ] **Vérifie ce qui va partir.** `git status` doit montrer tes scripts, ton README, ton `.gitignore` — et *pas* tes données. Si tu vois un `.csv` de 2 Go, corrige le `.gitignore` avant de continuer.
- [ ] **Premier commit :**
  ```bash
  git add .
  git commit -m "Premier commit : scripts et README"
  ```
- [ ] **Crée le dépôt sur GitHub et pousse, en une commande** (le dépôt est *privé*) :
  ```bash
  gh repo create mon-projet --private --source=. --push
  ```
- [ ] **Prends l'habitude.** Cette semaine, fais au moins trois commits avec un message qui dit *pourquoi*, et un `git push` à la fin de chaque journée.

**Le test.** Sur un autre ordinateur (ou dans un autre dossier), `git clone` ton dépôt. Tout le code est là ? Les données n'y sont pas ? C'est gagné.
