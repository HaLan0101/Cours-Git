#créer une branche  

$ git branch dev 

  

#afficher l’ensemble des branches 

$ git branch 

  

#déplacer le HEAD sur la branche mon_branche 

$ git checkout mon_branche 

  

#créer et déplacer le HEAD sur la branche mon_branche 

$ git checkout -b mon_branche  

  

#supprimer une branche 

$ git branch -d mon_branche  

  

#supprimer une branche qui n’est pas dans l’état “copie de l’espace de travail propre” 

$ git branch -D mon_branche  

  

#merger mon_branche dans autre_branche 

$ git merge mon_branche  

  

#merger même si on est dans une situation sans divergence de branche 

$ git merge dev --no-ff 

  

#lister toutes les branches non mergées 

$ git branch --no-merged 

  

#merger les modifications dans la branche HEAD 

$ git merge mon_branche --no-ff 

  

  

#permettre de faire la remise du code sur la branche où vous avez modifié votre code 

$ git stash 

  

#lister sur la branche les stash 

$ git stash list 

  

#recupérer ce qui était dans la stash ou un stash particulier 

$ git stash apply 

$ git stash apply stash@{n°} 

  

#récuperer les modifications de votre index 

$ git stash apply --index 

  

  

#enlever un stash particulier 

$ git stash drop stash@{n°} 

  

#créer de le dépot mon_fichier 

$ sh mon_fichier 

  

#marquer des commits spécifiques 

$ git tag -a v1.0 -m "message" 

  

  

#tag léger peu utilisé 

$ git tag v1 

  

#etiquetter après coup sur un commit donné 

$  git tag -a v1.0.1 -m "message" 9fceb2 

  

#lister les tags 

$ git tag 

  

#rechercher des tags particuliers 

$ git tag -l 'v8.*' 

  

#voir un tag annoté 

$ git show v8.2 

  

  

#se déplacer vers mon_dossier 

$ cd mon_doisser 

  

#créer un fichier 

$ mkdir mon_fichier 

  

#créer un dépôt vide nu sans répertoire de travail 

$ git --bare init 

  

#contenu du dossier 

$ branches config description HEAD hooks info objects refs 

  

#afficher une ligne dans mon_fichier 

$ echo "message" > mon_fichier 

  

#connecter le dépôt local à un serveur distant 

$ git remote add origin C:\Labs\my_lessons_server.git 

  

#push la branche master dans votre dépôt dans le serveur origin 

$ git push origin master 

  

#fusionner toutes les modifications présentes sur le dépôt distant dans le répertoire de travail local 

$ git pull origin master 

  

#lister les dépôts distants 

$ git remote 

  

#lister en mode verbeux 

$ git remote -v 

  

#ajouter un dépôt distant 

$ git remote add [alias] [chemin_du_serveur_distant] 

  

#supprimer un dépôt distant 

$ git remote rm [alias] 

  

#permettre de renommer votre dépôt distant 

$ git remote rename [alias] [new_alias] 

  

#extraire tous les fichiers du dépôt distant qui ne sont pas actuellement dans le répertoire de travail local. 

$ git fetch origin 

  

#comparer les différences entre master et local et distant 

$ git log master..origin/master 

  

  

#inspecter un dépôt distant 

$ git remote show origin 

  

#créez une clé ssh sur votre ordinateur 

$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com" 

  

#récupérez votre clé publique sur la machine 

$ cat ~/.ssh/id_rsa.pub 