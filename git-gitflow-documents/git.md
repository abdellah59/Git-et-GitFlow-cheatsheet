
=======
# 1. Git <div align="center">
  <img height="80" src="https://cours-web.ch/git/img/git-basics/git-logo.png" />
</div>
 

## 1.1 Introduction à Git

### 1.1.1 C'est quoi Git ?

Git est un outil de gestion de versions principalement utilisé pour suivre les modifications apportées à des fichiers, généralement du code, mais il peut aussi gérer d'autres types de fichiers. Plus précisément, il s'agit d'un système de contrôle de version décentralisé, ce qui signifie que chaque utilisateur possède une copie intégrale du projet.


### 1.1.2 Quelle différence existe-t-il entre Git et GitHub ?

<div align="center">
  <img height="150" src="https://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s1600/Github2.png" />
</div>
 

Git est le système de gestion de versions que tu utilises localement sur ton ordinateur pour gérer l’historique de ton code, créer des branches, et effectuer des commits.
GitHub est une plateforme web qui héberge des dépôts Git distants, permettant la collaboration à distance, la gestion de projets, et le partage de code entre plusieurs développeurs.
Les deux outils se complètent : tu utilises Git pour gérer ton code localement, et GitHub pour partager ce code avec d'autres et collaborer sur des projets.

## 1.2 Installation et configuration de Git

### 1.2.1 Installation de Git (windows, macOS, Linux)

Installation de Git

Windows :
Téléchargez l'installeur de Git depuis git-scm.com. Lancez l'installeur et suivez les étapes par défaut (vous pouvez personnaliser les options, mais les réglages par défaut sont généralement suffisants).

macOS :
Vous pouvez installer Git via Homebrew en utilisant la commande suivante dans le terminal :

```nginx
brew install git
```

Sinon, Git peut être installé en téléchargeant l'installeur depuis git-scm.com.

Linux :
Sur la plupart des distributions, Git peut être installé via le gestionnaire de paquets. Par exemple, sur Ubuntu/Debian :

```sql
sudo apt update
sudo apt install git
```
### 1.2.2 Paramétrage initial de Git (git config)

Une fois Git installé, vous devez configurer votre identité utilisateur. Cela se fait via les commandes git config :

Nom d'utilisateur :

```arduino
git config --global user.name "Votre Nom"
```

Adresse e-mail :

```nginx
git config --global user.email "votre.email@example.com"
```

### 1.2.3 Créer et associer une clé SSH

Pour une interaction sécurisée avec les dépôts distants (par exemple sur GitHub), vous pouvez configurer une clé SSH :

Générer une clé SSH :

```css
ssh-keygen -t rsa -b 4096 -C "votre.email@example.com"
```

Ajouter la clé SSH à votre agent :

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

Ajouter la clé publique à votre compte GitHub (ou autre service) :
Copiez la clé publique avec :

```bash
cat ~/.ssh/id_rsa.pub
```
Puis collez-la dans la section des clés SSH sur GitHub ou un autre service similaire.

Et voilà, Git est installé et configuré sur votre machine !

## 1.3 Les commandes de bases de Git

### 1.3.1 Créer un dépôt Git (git init)

La commande git init permet de créer un nouveau dépôt Git local dans un répertoire. Cela transforme le répertoire en un projet Git, prêt à être versionné.
Étapes pour créer un dépôt Git :

Accédez au répertoire de votre projet : Ouvrez votre terminal et naviguez vers le répertoire où vous souhaitez initialiser le dépôt.

```bash
cd /chemin/vers/votre/projet
```

Initialisez le dépôt Git : Exécutez la commande git init pour créer un dépôt Git dans le répertoire courant.

```bash
git init
```

Cela crée un sous-répertoire caché .git qui contient toute la configuration nécessaire à Git pour suivre l'historique des fichiers et des commits.

### 1.3.2 Cloner un dépôt existant (git clone)

Cloner un dépôt existant (git clone) - Résumé

La commande git clone permet de copier un dépôt Git distant (comme sur GitHub, GitLab, etc.) sur votre machine locale. Cela vous permet d'obtenir une copie complète du dépôt, y compris l'historique des commits, les branches et les tags.

Étapes pour cloner un dépôt Git :

Obtenez l'URL du dépôt distant : Allez sur la page du dépôt que vous souhaitez cloner (par exemple, sur GitHub) et copiez l'URL du dépôt. Cela peut ressembler à :
HTTPS : https://github.com/nom-utilisateur/nom-du-depot.git
SSH : git@github.com:nom-utilisateur/nom-du-depot.git

Clonez le dépôt avec git clone : Ouvrez votre terminal et tapez la commande suivante, en remplaçant <url-du-depot> par l'URL copiée :

```bash
git clone <url-du-depot>
```

Par exemple :

```bash
git clone https://github.com/nom-utilisateur/nom-du-depot.git
```

Naviguez dans le répertoire cloné : Une fois le dépôt cloné, un répertoire du nom du dépôt sera créé sur votre machine. Vous pouvez maintenant vous y rendre avec la commande cd :

```bash
git cd nom-du-depot
```

Vérifiez que le clonage a réussi : Vous pouvez vérifier que vous avez cloné correctement le dépôt en exécutant :

```bash
git status
```

### 1.3.3 Ajouter des fichiers au suivi (git add)

Ajouter des fichiers au dépôt : Une fois le dépôt initialisé, vous pouvez ajouter des fichiers avec la commande git add pour qu'ils soient suivis par Git.

```bash
git add
```

Cela ajoute tous les fichiers du répertoire. Vous pouvez également ajouter des fichiers spécifiques.

```bash
git add<fichier> ex: "git add readme.md"
```

### 1.3.4 Enregistrer les modifications (git commit)

Commitez les fichiers ajoutés :

```bash
git commit -m "Premier commit"
```

### 1.3.5 Vérifier l'état du dépôt (git status)

Vérifier l'état du dêpot :

```bash
git status
```

### 1.3.6 Consulter l'historique des commits (git log)

Consulter l'historique des commits (git log) - Résumé

La commande git log permet de visualiser l'historique des commits dans un dépôt Git. Elle affiche les commits effectués dans la branche actuelle, en montrant des informations telles que l'identifiant du commit, l'auteur, la date, et le message du commit.
Étapes pour consulter l'historique des commits :

Afficher l'historique des commits de la branche actuelle : Simplement exécuter la commande :

```bash
git log
```

Cela affichera une liste des commits, avec les informations suivantes pour chaque commit :


### 1.3.7 Annuler des modifications (git checkout, git reset)

1. Annuler des modifications non validées dans un fichier (git checkout)

La commande git checkout permet d'annuler des modifications locales dans un fichier et de le restaurer à son dernier état validé (commit).
Annuler les modifications dans un fichier spécifique :

Si vous avez modifié un fichier mais que vous n'avez pas encore fait de commit, vous pouvez annuler ces changements en utilisant :

```bash
git checkout -- <nom-du-fichier>
```
Note : Utiliser git checkout de cette manière affecte uniquement les fichiers modifiés non committés. Cela ne touche pas les fichiers ajoutés avec git add (mais pas encore committés).

2. Annuler les modifications dans la zone de staging (git reset)

La commande git reset permet de retirer un fichier de la zone de staging, c'est-à-dire d'annuler l'effet de git add. Si vous avez ajouté des fichiers au staging avec git add mais que vous ne souhaitez pas les inclure dans le commit suivant, vous pouvez utiliser git reset pour les retirer.
Retirer un fichier du staging :

```bash
git reset <nom-du-fichier>
```

Retirer tous les fichiers du staging :

Si vous avez ajouté plusieurs fichiers au staging et souhaitez tout retirer d'un coup :

```bash
git reset
```

3. Annuler un commit (git reset)

Si vous avez déjà fait un commit et que vous souhaitez l'annuler (ou revenir en arrière), vous pouvez utiliser git reset. Cette commande permet de réinitialiser l'historique des commits.
Réinitialiser au dernier commit mais garder les modifications :

Si vous souhaitez annuler le dernier commit tout en gardant les modifications dans vos fichiers (dans votre espace de travail), vous pouvez utiliser :

```bash
git reset --soft HEAD~1
```

Cela supprimera le dernier commit, mais les modifications seront toujours dans votre répertoire de travail et dans la zone de staging.
Réinitialiser au dernier commit et supprimer les modifications :

Si vous voulez annuler un commit et supprimer également les modifications associées, utilisez :

```bash
git reset --hard HEAD~1
```

Cela supprimera à la fois le dernier commit et toutes les modifications non validées.

Note : L'option --hard perd définitivement les modifications, alors assurez-vous d'avoir sauvegardé ce que vous souhaitez conserver avant d'utiliser cette option.