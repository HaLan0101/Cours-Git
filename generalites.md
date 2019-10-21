#s'enregistre dans .gitconfig de votre compte user 

$ git config --global user.name mon_nom 

$ git config --global user.email mon_email 

  

#définir un éditeur pour écrire le texte du commit 

$ git config --system core.editor vim 

  

#pour un dépôt en particulier, dans le fichier config du dossier .git/ 

$ git config --local user.name mon_nom 

$ git config --local user.email mon_email 

  

#initialiser un dépôt .git/ 

$ git init 

  

#voir le statut 

$ git status 

  

#ajouter à la staging area 

$ git add mon_fichier 

  

#arrêter de suivre un fichier mais ne pas l'effacer 

$ git rm --cached mon_fichier 

  

#permetre de voir comment Git crée  

$ find .git/objects -type f 

  

#commiter sans passer par l'éditeur de texte 

git commit -m "message" 

  

#enregistrer "commiter" les modifications, ouvrir l'éditeur et mettre un titre et texte plus long 

$ git commit 

  

#visualiser les logs, des informations relatives à chaque commit 

$ git log 

  

#visualiser les clés de hachages, les logs 

$ git log --oneline 

$ git shortlog 

  

#voir 5 derniers commits 

$ git log -5 

  

#log avec différence pour chaque commit sur les 5 derniers 

$ git log -p -5 

  

#stat sur les modifs par commits 

$ git log --stat 

  

#depuis deux semaines, --until existe également 

$ git log --since=2.weeks 

  

#trouver les commandes 

$ git help 

  

#voir alias dans la configuration 

$ git oneline 

  

#voir les différences entre deux branches 

$ git log master..origin/master 

  

#rechercher qui a fait les modifs par ligne -L 

$ git blame -L 40,60 mon_fichier 

  

#depuis 3 semaines avec auteurs des modifications 

$ git blame --since=3.weeks -- mon_fichier 

  

#rechercher avec expression régulière 

$ git blame -L "/^### /" mon_fichier 

  

#renommer un fichier 

git mv mon_ancien_fichier mon_nouveau_fichier 

  

#tout comiter sans passer par add 

git commit -a 

  

#effacer un fichier 

git rm mon_fichier 

  

#voir tous les fichiers suivis 

$ git ls-files 