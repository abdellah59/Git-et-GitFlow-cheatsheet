# Git & GitFlow Cheat Sheet

<div align="center">
  <img height="150" src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fmedium.com%2Fsoftware-incubator%2Fgit-and-github-a-beginners-guide-81fb984ce36a&psig=AOvVaw0pYQPHmgQ7YM2kS-42Fh_t&ust=1742479555227000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCMig-6iolowDFQAAAAAdAAAAABAE" />
</div>
 

Project Description
Ce document est un guide pratique pour comprendre et maîtriser Git et GitFlow. Que vous soyez un débutant découvrant les bases ou un utilisateur expérimenté cherchant à approfondir ses connaissances, cette cheat sheet aborde un large éventail de sujets essentiels.


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
   - [1.3.2 Cloner un dépôt existant (git clone)](git-gitflow-documents/git.md)
   - [1.3.3 Ajouter des fichiers au suivi (git add)](git-gitflow-documents/git.md)
   - [1.3.4 Enregistrer les modifications (git commit)](git-gitflow-documents/git.md)
   - [1.3.5 Vérifier l'état du dépôt (git status)](git-gitflow-documents/git.md)
   - [1.3.6 Consulter l'historique des commits (git log)](git-gitflow-documents/git.md)
   - [1.3.7 Annuler des modifications (git checkout, git reset)](git-gitflow-documents/git.md)


## 1.4 Les bases de Git

   - [1.4.1 Présentation des branches](git-gitflow-documents/git.md)
   - [1.4.2 Créer et naviguer entre les branches (git branch, git checkout, git switch) ](git-gitflow-documents/git.md)
   - [1.4.3 Fusionner des branches (git merge)](git-gitflow-documents/git.md)
   - [1.4.4 Résoudre les conflits de fusion](git-gitflow-documents/git.md)
   - [1.4.5 Envoyer des modifications vers un dépôt distant (git push)](git-gitflow-documents/git.md)
   - [1.4.6 Récupérer les modifications depuis un dépôt distant (git pull)](git-gitflow-documents/git.md)
   - [1.4.7 Collaborer avec des forks et des pull requests](git-gitflow-documents/git.md)



# 3. Cheat Sheet : Commandes principale 

Ce cheat sheet couvre les commandes essentielles pour **Git** et **GitFlow** afin de gérer efficacement les versions et le développement collaboratif.

<table>
    <thead>
        <tr>
            <th>Commande</th>
            <th>Fonction</th>
            <th>Exemple</th>
        </tr>   
    </thead>
    <tbody>
        <tr>
            <th colspan="3" align="left"> Mise en place & Initialisation</th>
        </tr>
        <tr>
            <td align="right"><code>git init</code></td>
            <td>Initialise un dépôt Git dans le dossier courant</td>
            <td></td>
        </tr>
         <tr>
            <td align="right"><code>git clone [url]</code></td>
            <td>Récupère l'entièreté d'un dépôt distant via URL</td>
            <td><code>git clone git@github.com:Simplon-hdf/cheats-sheets-git-flow.git</code></td>
        </tr>
        <tr>
            <th colspan="3" align="left">Index</th>
        </tr>
            <td align="right"><code>git status</code></td>
            <td>Affiche les fichiers modifiés dans le répertoire de travail</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git add [fichier]</code></td>
            <td>Déplace un fichier dans la zone de stage</td>
            <td><code>git add exemple.md</code></td>
        </tr>
        <tr>
            <td align="right"><code>git reset [fichier]</code></td>
            <td>Enlève un fichier de l'index tout en gardant les changements dans le répertoire de travail</td>
            <td><code>git reset exemple.md</code></td>
        </tr>
         <tr>
            <td align="right"><code>git diff</code></td>
            <td>Différence des changements en dehors de l'index</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git diff --staged</code></td>
            <td>Différence entre l'index et le dernier commit</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git diff [branche locale] [branche distante]</code></td>
            <td>Compare les différences entre une branche locale et distante</td>
            <td><code>git diff develop main</code></td>
        </tr>
        <tr>
            <td align="right"><code>git commit -m [message]</code></td>
            <td>Effectue le commit contenant les fichiers dans l'index</td>
            <td><code>git commit -m "Renamed exemple.md"</code></td>
        </tr>
        <tr>
            <th colspan="3" align="left">Branches</th>
        </tr>
        <tr>
            <td align="right"><code>git branch -av</code></td>
            <td>Liste les branches. Un * apparaîtra à côté de la branche actuelle</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git branch [branche]</code></td>
            <td>Créer une nouvelle branche</td>
            <td><code>git branch main</code></td>
        </tr>
        <tr>
            <td align="right"><code>git switch [branche]</code></td>
            <td>Change la branche courante</td>
            <td><code>git switch develop</code></td>
        </tr>
        <tr>
            <td align="right"><code>git branch -d [branche]</code></td>
            <td>Supprime la branche locale</td>
            <td><code>git branch -d develop</code></td>
        </tr>
        <tr>
            <td align="right"><code>git checkout --track</code></td>
            <td>Créer une nouvelle branche locale à partir d'une branche distante, et la suivre</td>
            <td></td>
        <tr>
            <td align="right"><code>git tag [tag-name]</code></td>
            <td>Créer un tag sur le commit actuel</td>
            <td><code>git tag v1.0</code></td>
        </tr>
        </tr>
        <tr>
            <th colspan="3" align="left">Historique</th> 
        </tr>
        <tr>
            <td align="right"><code>git log</code></td>
            <td>Affiche l'historique des commits</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git log -p [fichier]</code></td>
            <td>Affiche l'historique des commits sur un fichier spécifique</td>
            <td><code>git log -p exemple.md</code></td>
        </tr>
        <tr>
            <td align="right"><code>git blame [fichier]</code></td>
            <td>Affiche l'historique des modifications, y compris l'auteur sur un fichier spécifique</td>
            <td><code>git blame exemple.md</code></td>
        </tr>
        <tr>
            <th colspan="3" align="left">Mise à jour et publication</th>
        </tr>
        <tr>
            <td align="right"><code>git remote -v</code></td>
            <td>Liste les remote configurés</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git remote show [remote]</code></td>
            <td>Affiche les informations de la remote</td>
            <td><code>git remote show origin</code></td>
        </tr>
        <tr>
            <td align="right"><code>git remote add [remote] [url]</code></td>
            <td>Permet de créer une connexion avec un dépôt distant sous un raccourci</td>
            <td><code>git remote add origin git@github.com:Simplon-hdf/cheats-sheets-git-flow.git</code></td>
        </tr>
        <tr>
            <td align="right"><code>git fetch [remote]</code></td>
            <td>Récupère toutes les modifications de la remote sans fusionner les changements</td>
            <td><code>git fetch origin</code></td>
        </tr>
        <tr>
            <td align="right"><code>git pull [remote] [branche]</code></td>
            <td>Récupère les modifications de la branche, et les fusionne</td>
            <td><code>git pull origin main</code></td>
        </tr>
        <tr>
            <td align="right"><code>git push [remote] [branche]</code></td>
            <td>Pousse les commits d'une branche locale vers un dépôt distant</td>
            <td><code>git push origin main</code></td>
        </tr>
        <tr>
            <th colspan="3" align="left">Fusionner & Rebaser</th>
        </tr>
        <tr>
            <td align="right"><code>git merge [branche]</code></td>
            <td>Fusionne la branche spécifiée avec la branche actuelle</td>
            <td><code>git merge main</code></td>
        </tr>
        <tr>
            <td align="right"><code>git rebase [branche]</code></td>
            <td>Réapplique l'historique des commits de la branche actuelle au dessus de la branche spécifiée</td>
            <td><code>git rebase main</code></td>
        </tr>
        <tr>
            <td align="right"><code>git rebase --abort</code></td>
            <td>Annule le processus de rebase en cours</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git rebase --continue</code></td>
            <td>Poursuit le processus de rebase après la résolution des conflits</td>
            <td></td>
        </tr>
        <tr>
            <td align="right"><code>git mergetool</code></td>
            <td>Ouvre un outil de fusion pour résoudre les conflits</td>
            <td></td>
        </tr>
        <tr>
            <th colspan="3" align="left"    >Rétablir/Annuler</th>
        </tr>
        <tr>
            <td align="right"><code>git reset --hard HEAD</code></td>
            <td>Réinitialise l'index et le répertoire de travail au commit référencé par HEAD</td>
            <td><code>git reset --hard @~1</code></td>
        </tr>
        <tr>
            <td align="right"><code>git checkout HEAD [fichier]</code></td>
            <td>Restaure un fichier spécifique dans le répertoire de travail au dernier commit (HEAD)</td>
            <td><code>git checkout HEAD exemple.md</code></td>
        </tr>
        <tr>
            <td align="right"><code>git revert [commit]</code></td>
            <td>Annule les modifications d'un commit spécifique</td>
            <td><code>git revert 8d6fe82</code></td>
        </tr>
        <tr>
            <td align="right"><code>git reset --hard [commit]</code></td>
            <td>Réinitialise l'index et le répertoire de travail au commit spécifié</td>
            <td><code>git reset --hard 8d6fe82</code></td>
        </tr>
        <tr>
            <td align="right"><code>git reset [commit]</code></td>
            <td>Déplace la branche actuelle vers le commit spécifié</td>
            <td><code>git reset 8d6fe82</code></td>
        </tr>
        <tr>
            <td align="right"><code>git reset --keep [commit]</code></td>
            <td>Déplace la branche tout en conservant les modifications en dehors de l'index </td>
            <td><code>git reset --keep 8d6fe82</code></td>
        </tr>
    </tbody>

</table>


