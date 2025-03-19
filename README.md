# Git & GitFlow Cheat Sheet

Ce cheat sheet couvre les commandes essentielles pour **Git** et **GitFlow** afin de gérer efficacement les versions et le développement collaboratif.

## Table des matières

# 1. Git
### 1.1 Introduction à Git

   - [1.1.1 C'est quoi Git ? ](git-gitflow-documents/git.md)
   - [1.1.2 Pourquoi adopter Git ? ](git-gitflow-documents/git.md)
   - [1.1.3 Comment utiliser Git au quotidien ?](git-gitflow-documents/git.md)
   - [1.1.4 Quelle différence existe-t-il entre Git et GitHub ?](git-gitflow-documents/git.md)

## 1.2 Installation et configuration de Git

   - [1.2.1 Installation et configuration de Git (windows, macOS, Linux)](git-gitflow-documents/git.md)
   - [1.2.2 Paramétrage initial de Git (git config)](git-gitflow-documents/git.md)
   - [1.2.3 Créer et associer une clé SSH](git-gitflow-documents/git.md)

## 1.3 Les bases de Git

   - [1.3.1 Créer un dépôt Git (git init)](git-gitflow-documents/git.md)
   - [1.3.2 Cloner un dépôt existant (git clone) ](git-gitflow-documents/git.md)
   - [1.3.3 Ajouter des fichiers au suivi (git add)](git-gitflow-documents/git.md)
   - [1.3.1 Enregistrer les modifications (git commit)](git-gitflow-documents/git.md)
   - [1.3.2 Vérifier l'état du dépôt (git status) ](git-gitflow-documents/git.md)
   - [1.3.3 Consulter l'historique des commits (git log)](git-gitflow-documents/git.md)
   - [1.3.3 Annuler des modifications (git checkout, git reset)](git-gitflow-documents/git.md)
Git-et-GitFlow-cheatsheet 

## 1.4 Les bases de Git

   - [1.4.1 Présentation des branches](git-gitflow-documents/git.md)
   - [1.4.2 Créer et naviguer entre les branches (git branch, git checkout, git switch) ](git-gitflow-documents/git.md)
   - [1.4.3 Fusionner des branches (git merge)](git-gitflow-documents/git.md)
   - [1.4.1 Résoudre les conflits de fusion](git-gitflow-documents/git.md)
   - [1.4.2 Envoyer des modifications vers un dépôt distant (git push)](git-gitflow-documents/git.md)
   - [1.4.3 Récupérer les modifications depuis un dépôt distant (git pull)](git-gitflow-documents/git.md)
   - [1.4.3 Collaborer avec des forks et des pull requests](git-gitflow-documents/git.md)

# 2. GitFlow

## 2.1 Guide Complet sur GitFlow

   - [2.1.1 Qu'est-ce qu'un workflow](git-gitflow-documents/gitflow.md)
   - [2.1.2 Qu'est-ce que GitFlow ?](git-gitflow-documents/gitflow.md)
   - [2.1.3 Pourquoi utiliser GitFlow ?](git-gitflow-documents/gitflow.md)
   - [2.1.4 Différence entre Git et GitFlow](git-gitflow-documents/gitflow.md)
   - [2.1.5 Avantages et inconvénients de GitFlow](git-gitflow-documents/gitflow.md)

## 2.2 Installation de GitFlow

   - [2.2.1 Prérequis](git-gitflow-documents/gitflow.md)
   - [2.2.2 Installation sur Linux (Debian/Ubuntu)](git-gitflow-documents/gitflow.md)
   - [2.2.3 Installation sur macOS (via Homebrew)](git-gitflow-documents/gitflow.md)
   - [2.2.4 Installation sur Windows](git-gitflow-documents/gitflow.md)
   - [2.2.5 Vérifier l'installation](git-gitflow-documents/gitflow.md)
   
## 2.3 Initialisation de GitFlow dans un projet
   
## 2.4 Utilisation des branches GitFlow
   - [2.4.1 Gestion des fonctionnalités (features)](git-gitflow-documents/gitflow.md)
   - [2.4.2 Gestion des versions (releases)](git-gitflow-documents/gitflow.md)
   - [2.4.3 Gestion des correctifs (hotfixs)](git-gitflow-documents/gitflow.md)
   
## 2.5 Commandes avancées et bonnes pratiques

   - [2.5.1 Comment annuler une action GitFlow](git-gitflow-documents/gitflow.md)
   - [2.5.2 Personnaliser GitFlow](git-gitflow-documents/gitflow.md)
   
## 2.6 Problèmes courants et solutions

  - [2.6.1 Conflits entre branches](git-gitflow-documents/gitflow.md)
  - [2.6.2 Rebase et merge dans GitFlow](git-gitflow-documents/gitflow.md)

## 2.7 Conclusion

  - [2.7.1 Quand utiliser GitFlow ?](git-gitflow-documents/gitflow.md)
  - [2.7.2 Résumé des bonnes pratiques](git-gitflow-documents/gitflow.md)



### Configuration de Git
```bash
# Configurer le nom et l'email
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"

# Vérifier la configuration
git config --list
