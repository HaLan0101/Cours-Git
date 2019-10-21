#afficher les 3 derniers commits et sortir de la commande 

$ git --no-pager log --oneline -n 3 

  

#consulter les deux derniers commit 

$ git log --oneline -2 

  

#consulter les commits d’un auteur 

$ git log --author "nom_author" 

  

#consulter les commits avant le 01 sept 2019 

$ git log --before="2019-09-01" 

  

#visualiser les modifications dans l'ensemble des commits 

$ git log -p 

  

#visualiser les modifications dans les 2 derniers commit 

$ git log -2 -p 

  

#permettre de rechercher des logs (messages des commits): E expression pour rechercher les/l’occurence(s) et i pour insensible à la casse (majuscule/minuscule)  

$ git log -E -i --grep='message' 

  

#savoir qui a fait des modifications, l'heure et la date,... sur mon_fichier 

$ git blame mon_fichier 

  

#afficher les modifications dans le WD & l’index 

$ git diff 

  

#afficher les différences entre le dernier commit et l’index 

$ git diff --cached 

  

#voir les différences après avoir commité les changements, HEAD~1 pour reculer d’un commit en arrière 

$ git diff HEAD~1 

  

#visualiser les différences entre le HEAD et un état antérieur du dépôt, par exemple 3 commits avant 

$ git diff HEAD~3 HEAD 

  

#voir les modifications entre deux commits via les haches 

$ git log hache_1 hache_2 

  

#faire des stat sur les différences opérées dans les fichiers 

$ git diff --stat 

  

#remettre le dépôt dans l’état dans lequel il se trouvait juste avant la modification 

$ git restore mon_fichier 

  

#refaire la modification et que l’on ajoute le fichier dans l’index 

$ git restore --staged 

  

#créer un nouveau commit avec le même parent que le commit courant 

$ git commit -m "message" --amend 

  

#changer uniquement le message du dernier commit 

$ git commit "un message" --amend --no-edit 

  

#annuler le dernier commit et mettre tout dans le WD sans perte (revient au commit précédent -1) 

$ git reset HEAD~1 

  

#annuler le dernier commit et mettre tout dans la staging area sans perte 

$ git reset --soft HEAD~1 

  

#le HEAD -> master se déplacera sur le commit 8ef0ef2 en annulant les autres 

commits (messages) sans perte (sans perdre votre travail) 

$ git reset 8ef0ef2 

  

#annuler le dernier commit et supprimer les modifications(danger) 

$ git reste –hard HEAD~1 

  

  

#permetre de revenir avant la refonte 

$ git checkout 9b85968 mon_fichier 