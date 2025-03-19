# 1. Git

## 1.1 Introduction à Git

### 1.1.1 C'est quoi Git ?

Décentralisation : Contrairement aux systèmes de gestion de version centralisés, Git permet à chaque développeur de disposer de sa propre copie complète du projet, avec tout l'historique des modifications. Cela signifie qu'il est possible de travailler de manière autonome sans avoir besoin d'une connexion réseau constante.

Suivi des versions : Git garde une trace de chaque modification apportée aux fichiers d'un projet, ce qui permet de revenir facilement à des versions antérieures, de voir quelles modifications ont été effectuées, et par qui.

Branches : Git permet de travailler sur des branches distinctes, ce qui permet de tester de nouvelles fonctionnalités, de corriger des bugs, ou d'expérimenter sans affecter le code principal. Ces branches peuvent ensuite être fusionnées une fois terminées.

Collaboratif : Git facilite la collaboration entre plusieurs développeurs. Les changements de chacun peuvent être intégrés (fusionnés) dans le projet principal, et Git gère les conflits de manière efficace en permettant aux développeurs de résoudre les divergences manuellement ou automatiquement.

Performance : Git est conçu pour être rapide et efficace, même pour de très grands projets. La plupart des opérations (comme le commit, le checkout ou le merge) sont effectuées localement, ce qui les rend plus rapides.

### 1.1.2 Pourquoi adopter Git ? 

Décentralisation : Contrairement aux systèmes de gestion de version centralisés, Git permet à chaque développeur de disposer de sa propre copie complète du projet, avec tout l'historique des modifications. Cela signifie qu'il est possible de travailler de manière autonome sans avoir besoin d'une connexion réseau constante.

Suivi des versions : Git garde une trace de chaque modification apportée aux fichiers d'un projet, ce qui permet de revenir facilement à des versions antérieures, de voir quelles modifications ont été effectuées, et par qui.

Branches : Git permet de travailler sur des branches distinctes, ce qui permet de tester de nouvelles fonctionnalités, de corriger des bugs, ou d'expérimenter sans affecter le code principal. Ces branches peuvent ensuite être fusionnées une fois terminées.

Collaboratif : Git facilite la collaboration entre plusieurs développeurs. Les changements de chacun peuvent être intégrés (fusionnés) dans le projet principal, et Git gère les conflits de manière efficace en permettant aux développeurs de résoudre les divergences manuellement ou automatiquement.

Performance : Git est conçu pour être rapide et efficace, même pour de très grands projets. La plupart des opérations (comme le commit, le checkout ou le merge) sont effectuées localement, ce qui les rend plus rapides.

### 1.1.3 Comment utiliser Git au quotidien ?

Git suit les modifications sous forme de commits. Chaque commit est une sorte de "photo" de l'état de ton projet à un moment donné. Ces commits sont organisés de manière à pouvoir reconstruire l'historique complet du projet.

Voici un aperçu du fonctionnement de Git :

- Dépôt local et dépôt distant :
  Un dépôt Git (repository ou repo) est l'endroit où Git stocke les fichiers du projet et l'historique des modifications. Chaque utilisateur a une copie locale du dépôt.
  Les équipes partagent souvent un dépôt distant (comme sur GitHub ou GitLab), qui est une version centralisée du projet.

- Travail local :
  Travailler localement signifie que tu peux apporter des modifications à ton dépôt sans être connecté à un dépôt distant.
  Une fois que tu es satisfait de tes changements, tu les commits pour sauvegarder tes modifications dans l'historique local.

- Synchronisation avec le dépôt distant :
  Une fois les changements commis localement, tu peux utiliser des commandes comme git push pour envoyer tes modifications au dépôt distant.
  Tu peux aussi utiliser git fetch ou git pull pour récupérer les modifications faites par d'autres contributeurs depuis le dépôt distant.

### 1.1.4 Quelle différence existe-t-il entre Git et GitHub ?

Git est le système de gestion de versions que tu utilises localement sur ton ordinateur pour gérer l’historique de ton code, créer des branches, et effectuer des commits.
GitHub est une plateforme web qui héberge des dépôts Git distants, permettant la collaboration à distance, la gestion de projets, et le partage de code entre plusieurs développeurs.
Les deux outils se complètent : tu utilises Git pour gérer ton code localement, et GitHub pour partager ce code avec d'autres et collaborer sur des projets.

## 1.2 Installation et configuration de Git

### 1.2.1 Installation et configuration de Git (windows, macOS, Linux)

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

Configuration initiale de Git

Une fois Git installé, vous devez configurer votre identité utilisateur. Cela se fait via les commandes git config :

Nom d'utilisateur :

```arduino
git config --global user.name "Votre Nom"
```

Adresse e-mail :

```nginx
git config --global user.email "votre.email@example.com"
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