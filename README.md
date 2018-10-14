# Branches
Pour une branche ,on peut executer pusieurs commits comme il est aussi possible de realiser un meme commit sur plusieurs branches.

## Création d'une branche 
il est recommandé de créér en premier un dépôt distant et le récuperer en local envue d'y créer des branches, autre que le master.
on utilise la commande ** git branch nom_branche** pour en créer une .

![](""C:/Users/skeita/Desktop/Branches/creation_branche.PNG")

## fusion des commits dans deux branches distantes

pour exécuter des commits dans une branche autre que le master ,il faut y prealablement acceder par la commande 
**git checkout "nom_branche"** puis faire des modifications puis des commits par la commande classique **git commit -a**.
pour fusionner  ces commits dans la branche  master,il faut retourner dans cette branche puis utiliser la commande
**git merge 'autre branche que le master".

![](""C:/Users/skeita/Desktop/Branches/comit_branches_b1_merges_branches.PNG")



Envoyez la branche b1 sur le serveur et vérifiez que vous la voyez sur la page web du serveur.
Créez une branche b2 à partir du commit précédant le master courant, faites quelques commits dans b2 puis fusionnez-les dans le master.
Fusionnez le master dans b1 et vérifiez le graphe des commits avec le client Git console et avec un client graphique.
Envoyez la branche b2 sur le serveur puis supprimez-la sur le dépôt local puis sur le dépôt distant.
