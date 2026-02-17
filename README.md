# Évaluation Git & GitHub
Projet réalisé dans le cadre d'une évaluation Git & GitHub.
## Auteur : Chiara
## Technologies utilisées
- HTML
- CSS
- Git
- GitHub

# Partie 1 - Git en local

Création du projet : 
cd git-github-evaluation
git init
git status
![alt text](image.png)

Premier fichier et premier commit:
git add README.md
git status
git commit -m "add readme"

Ajout de fichiers et commits multiples:
git status
![alt text](image-1.png)
git add index.html style.css
git commit -m "add index & style"
![alt text](image-2.png)

Gestion de l'historique et correction de commits:
git add README.md
git diff --staged
![alt text](image-3.png)
git commit -m "add author readme"
git log --oneline
![alt text](image-4.png)
git show HEAD
![alt text](image-5.png)

Travail avec les branches:
git checkout -b feature/ajout-style
git branch
![alt text](image-6.png)
git add style.css
git commit -m "improve style"
git checkout master
git merge feature/ajout-style
git branch -d feature/ajout-style
git log --oneline --graph
![alt text](image-7.png)

# Partie 2 - Github

Création du dépôt GitHub:
![alt text](image-8.png)

Lien entre dépôt local et distant:
git remote add origin https://github.com/ChiaraGinelli/git-github-evaluation.git
git remote -v
![alt text](image-9.png)

Envoi du projet sur GitHub:
git push -u origin master
![alt text](image-10.png)

Gestion des branches distantes:
git checkout -b feature/page-contact
git add contact.html
git commit -m "add contact page"
git push -u origin feature/page-contact
![alt text](image-11.png)
git checkout master
git merge feature/page-contact
git push
![alt text](image-12.png)
git push origin --delete feature/page-contact
git log --oneline --graph
![alt text](image-13.png)

Pull Request & GitHub Flow:
git checkout -b feature/amelioration-readme
