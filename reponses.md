# Réponses TP3 - Git

## Exo 1 : Branches  
1. git branch feature-1, git branch feature-2  
2. git branch  
3. git checkout feature-1  
4. Modif README.md + git add . && git commit -m "Modif feature-1"  
5. git checkout main, cat README.md  

## Exo 2 : Fusion  
1. git branch dev && git checkout dev  
2. echo "Note" > notes.txt && git add . && git commit -m "Ajout note"  
3. git checkout main && git merge dev  
4. ls pour vérifier  
5. git branch -d dev  

## Exo 3 : Conflits  
1. git branch conflit-test && git checkout conflit-test  
2. Modif README.md sur main : "Version Main" + commit  
3. Modif README.md sur conflit-test : "Version Test" + commit  
4. git checkout main && git merge conflit-test  
5. Résolution : "Version Main et Test" + git add . && git commit -m "Résolution conflit"  

## Exo 4 : Rebase  
1. git branch feature-rebase && git checkout feature-rebase  
2. echo "Contenu" > feature.txt && git add . && git commit -m "Ajout feature.txt" (plusieurs commits)  
3. Sur main, modif fichier + commit  
4. git checkout feature-rebase && git rebase main  
5. git log --oneline --graph  

## Exo 5 : Historique  
1. git branch feature-a feature-b feature-c  
2. Dans chaque branche, ajout de fichiers + 2 commits  
3. git checkout main && git merge feature-a feature-b feature-c  
4. git log --all --decorate --oneline --graph, git branch -v  
* 0ee94e4 Sauvegarde avant rebase
* 8f85b25 Ajout d'une deuxième ligne dans feature.txt
* 9e87f86 Ajout du fichier feature.txt
* ff793e0 Mise à jour du fichier main.txt
* faa59cd Ajout du fichier main.txt
*   7ff2545 Résolution du conflit : fusion des versions Main et Test
|\  
| * 6958e53 Modification du README sur conflit-test
* | fad0790 Modification du README sur main
|/  
* e8ea874 ajout du fichier notes
* 2f2e79d 1.2
* ef117ef Premier commit : création du README
