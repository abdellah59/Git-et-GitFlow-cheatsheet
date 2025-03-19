# Git & GitFlow Cheat Sheet

Ce cheat sheet couvre les commandes essentielles pour **Git** et **GitFlow** afin de gérer efficacement les versions et le développement collaboratif.

## Table des matières

# 1. Git
### 1.1 Introduction à Git

   - [1.1.1 C'est quoi Git ? ](introduction-a-git.md)
   - [1.1.2 Pourquoi adopter Git ? ](introduction-a-git.md)
   - [1.1.3 Comment utiliser Git au quotidien ?](introduction-a-git.md)
   - [1.1.4 Quelle différence existe-t-il entre Git et GitHub ?](git/introduction-a-git.md)

## 1.2 Installation et configuration de Git

   - [1.2.1 Installation et configuration de Git (windows, macOS, Linux)](installation-et-configuration-de-git.md)
   - [1.2.2 Paramétrage initial de Git (git config)](installation-et-configuration-de-git.md)
   - [1.2.3 Créer et associer une clé SSH](installation-et-configuration-de-git.md)

## 1.3 Les bases de Git

   - [1.3.1 Créer un dépôt Git (git init)](.git/configuration-de-git.md)
   - [1.3.2 Cloner un dépôt existant (git clone) ](#commandes-de-base)
   - [1.3.3 Ajouter des fichiers au suivi (git add)](#travailler-avec-des-branches)
   - [1.3.1 Enregistrer les modifications (git commit)](.git/configuration-de-git.md)
   - [1.3.2 Vérifier l'état du dépôt (git status) ](#commandes-de-base)
   - [1.3.3 Consulter l'historique des commits (git log)](#travailler-avec-des-branches)
   - [1.3.3 Annuler des modifications (git checkout, git reset)](#travailler-avec-des-branches)


## 1.4 Les bases de Git

   - [1.4.1 Présentation des branches](.git/configuration-de-git.md)
   - [1.4.2 Créer et naviguer entre les branches (git branch, git checkout, git switch) ](#commandes-de-base)
   - [1.4.3 Fusionner des branches (git merge)](#travailler-avec-des-branches)
   - [1.4.1 Résoudre les conflits de fusion](.git/configuration-de-git.md)
   - [1.4.2 Envoyer des modifications vers un dépôt distant (git push)](#commandes-de-base)
   - [1.4.3 Récupérer les modifications depuis un dépôt distant (git pull)](#travailler-avec-des-branches)
   - [1.4.3 Collaborer avec des forks et des pull requests](#travailler-avec-des-branches)

### Configuration de Git
```bash
# Configurer le nom et l'email
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"

# Vérifier la configuration
git config --list
