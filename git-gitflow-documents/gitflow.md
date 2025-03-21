# 2. Guide Complet sur GitFlow

<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--b_QCE-F_--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://my-bucket-image2.s3.amazonaws.com/ImageGitHub/git-flow-logo.png" width="400" />

## 2.1 Guide Complet sur GitFlow

   - [2.1.1 Qu'est-ce qu'un workflow](#211-quest-ce-quun-workflow)
   - [2.1.2 Qu'est-ce que GitFlow ?](#212-quest-ce-que-gitflow-)
   - [2.1.3 Pourquoi utiliser GitFlow ?](#213-pourquoi-utiliser-gitflow-)
   - [2.1.4 Différence entre Git et GitFlow](#214-différence-entre-git-et-gitflow)
   - [2.1.5 Avantages et inconvénients de GitFlow](#215-avantages-et-inconvénients-de-gitflow)

## 2.2 Installation de GitFlow

   - [2.2.1 Prérequis](#221-prérequis)
   - [2.2.2 Installation sur Linux (Debian/Ubuntu)](#222-installation-sur-linux-debianubuntu)
   - [2.2.3 Installation sur macOS (via Homebrew)](#223-installation-sur-macos-via-homebrew)
   - [2.2.4 Installation sur Windows](#224-installation-sur-windows)
   - [2.2.5 Vérifier l'installation](#225-vérifier-linstallation)
   
## 2.3 Initialisation de GitFlow dans un projet
   
## 2.4 Utilisation des branches GitFlow
   - [2.4.1 Gestion des fonctionnalités (features)](#241-gestion-des-fonctionnalités-features)
   - [2.4.2 Gestion des versions (releases)](#242-gestion-des-versions-releases)
   - [2.4.3 Gestion des correctifs (hotfixs)](#243-gestion-des-correctifs-hotfixs)
   
## 2.5 Commandes avancées et bonnes pratiques

   - [2.5.1 Comment annuler une action GitFlow](#251-comment-annuler-une-action-gitflow)
   - [2.5.2 Personnaliser GitFlow](#252-personnaliser-gitflow)
   
## 2.6 Problèmes courants et solutions

  - [2.6.1 Conflits entre branches](#261-conflits-entre-branches)
  - [2.6.2 Rebase et merge dans GitFlow](#262-rebase-et-merge-dans-gitflow)

## 2.7 Conclusion

  - [2.7.1 Quand utiliser GitFlow ?](#271-quand-utiliser-gitflow-)
  - [2.7.2 Résumé des bonnes pratiques](#272-résumé-des-bonnes-pratiques)
## 2.1 Introduction à GitFlow

## 2.1.1 Qu'est ce qu'un workflow

<div style="text-align: center;">
  <img src="https://imgur.com/DglXdMo.png" width="150" />
</div>

Un **workflow** est une série de processus ou d'étapes organisées de manière logique pour accomplir une tâche ou un objectif spécifique. Dans le contexte de Git, un workflow définit la manière dont les développeurs collaborent sur un projet en utilisant des branches, des merges, et des pratiques spécifiques pour gérer le code source de manière efficace et structurée.


### 2.1.2 Qu'est-ce que GitFlow ?
**GitFlow** est un workflow Git qui définit un ensemble de règles et de pratiques pour organiser le développement de logiciels à l'aide de branches. Il introduit des branches spécifiques pour gérer les fonctionnalités, les versions et les corrections de bugs de manière structurée.


### 2.1.3 Pourquoi utiliser GitFlow ?
- Facilite la gestion des versions et du développement collaboratif.
- Clarifie les rôles des différentes branches.
- Permet une meilleure organisation des mises en production.

### 2.1.4 Différence entre Git et GitFlow
Git est un système de contrôle de version, tandis que GitFlow est une méthodologie pour l’utiliser efficacement.

### 2.1.5 Avantages et inconvénients de GitFlow
- Bonne gestion des versions 
- Adapté aux projets complexes 
- Peut être trop lourd pour des projets simples

---

## 2.2 Installation de GitFlow

### 2.2.1 Prérequis
- Git doit être installé sur votre machine.

### 2.2.2 Installation sur Linux (Debian/Ubuntu)
```bash
sudo apt update && sudo apt install git-flow
```

### 2.2.3 Installation sur macOS (via Homebrew)
```bash
brew install git-flow-avh
```

### 2.2.4 Installation sur Windows
```powershell
scoop install git-flow-avh
```

### 2.2.5 Vérifier l'installation
```bash
git flow version
```

---

## 2.3 Initialisation de GitFlow dans un projet

Dans votre dépôt Git, exécutez :
```bash
git flow init
```
Répondez aux questions pour configurer les branches :
- Branche principale (`main`)
- Branche de développement (`develop`)
- Préfixes pour features, releases, hotfixes

---

## 2.4 Utilisation des branches GitFlow

### 2.4.1 Gestion des fonctionnalités (features)
Créer une nouvelle feature :
```bash
git flow feature start nom-de-la-feature
```
Finaliser une feature :
```bash
git flow feature finish nom-de-la-feature
```

### 2.4.2 Gestion des versions (releases)
Créer une release :
```bash
git flow release start 1.0.0
```
Finaliser une release :
```bash
git flow release finish 1.0.0
```

### 2.4.3 Gestion des correctifs (hotfixs)
Créer un hotfix :
```bash
git flow hotfix start fix-urgent
```
Finaliser un hotfix :
```bash
git flow hotfix finish fix-urgent
```

---

## 2.5 Commandes avancées et bonnes pratiques

### 2.5.1 Comment annuler une action GitFlow
- Annuler une feature :
```bash
git flow feature delete nom-de-la-feature
```
- Annuler une release :
```bash
git flow release delete 1.0.0
```

### 2.5.2 Personnaliser GitFlow
Modifier les préfixes des branches via `.git/config`.

---

## 2.6 Problèmes courants et solutions

### 2.6.1 Conflits entre branches
Utiliser `git merge` ou `git rebase` pour résoudre les conflits.

### 2.6.2 Rebase et merge dans GitFlow
- `git rebase develop` pour mettre à jour une feature.
- `git merge --no-ff` pour conserver l’historique.

---

## 2.7 Conclusion

<div style="text-align: center;">
  <img src="https://imgur.com/6XjrkCx.png" width="150" />
</div>

### 2.7.1 Quand utiliser GitFlow ?
- Projets complexes avec plusieurs versions en parallèle.
- Développement en équipe.

### 2.7.2 Résumé des bonnes pratiques
✔️ Utiliser `develop` pour les nouvelles features.  
✔️ Créer des branches `release/*` avant la mise en production.  
✔️ Corriger les bugs urgents via `hotfix/*`.  

GitFlow est un outil puissant pour structurer vos workflows Git !
