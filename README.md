# Branches
Pour une branche ,on peut executer pusieurs commits comme il est aussi possible de stocker un meme commit dans  plusieurs branches.

## Création d'une branche 
il est recommandé de créér en premier un dépôt distant et le récuperer en local envue d'y créer des branches, autre que le master.
on utilise la commande ** git branch nom_branche** pour en créer une .

![](""C:/Users/skeita/Desktop/Branches/creation_branche.PNG")

## fusion des commits dans deux branches distantes

pour exécuter des commits dans une branche autre que le master ,il faut y prealablement acceder par la commande 
**git checkout "nom_branche"** puis faire des modifications puis des commits par la commande classique **git commit -a**.
pour fusionner  ces commits dans la branche  master,il faut retourner dans cette branche puis utiliser la commande
**git merge 'autre branche que le master".

![]("C:/Users/skeita/Desktop/Branches/comit_branches_b1_merges_branches.PNG")

Envoie d'une branche sur le serveur et vérification de sa présence sur la page web du serveur.
pour envoyer une branche autre que le master,créée en local ,on se positionne dans cette branche puis on uilise la commande
** git push --set-upstream origin "nom_branche"**

![]("C:/Users/skeita/Desktop/Branches/push_b1.PNG")

Il suffit d'utiliser la commande **git ls-remote** pour verfier si la branche pushée existe dans la liste des branches distantes.

![](""C:/Users/skeita/Desktop/Branches/verication_pushBranche.PNG")

## Création d'une nouvelle branche "b2" à partir du commit précédant dans le master courant,fusion de quelques commits dans b2  dans le master.
Il faudrait retourner au commit precédent du master(avant la fusion avec les modication d'une autre branche)par la commande 
**git checkout --** puis créer la nouvelle branche dans le master (**git branch "nom_branche"**).Une fois des commits realisés dans la nouvelle branche sur des modifications, on peut utiliser la commande **git merge "nom_branche** dans le master.

![](""C:/Users/skeita/Desktop/Branches/b3_merge.PNG")

Fusion la branche  master dans b1 et vérifiez le graphe des commits avec le client Git console et avec un client graphique.
Envoyez la branche b2 sur le serveur puis supprimez-la sur le dépôt local puis sur le dépôt distant.
