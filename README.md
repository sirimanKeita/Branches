# Branches
plusieurs commits peuvent etre reéalisées dans une  même branche.Iversement plusieurs branches d'un même dépot  peuvent conténir le même commit.La branche Master est celle par défaut,initialement associée à un dépôt.En plus de cette branche initiale,le dépôt peut avoir plusieurs branches qui qui permettent de gerer individuellement les sous parties d'un projet.Elles présentent l'avantage de pouvoir les merger par la suite.

## Création d'une branche 
Il est recommandé de créér en premier un dépôt distant et de le récuperer en local envue d'y créer des branches, autre que le master.On utilise la commande **git branch nom_branche** pour en créer une.

![](""C:/Users/skeita/Desktop/Branches/creation_branche.PNG")


## Fusion des commits réalisées dans deux branches différentes

Pour exécuter des commits dans une branche autre que le master,il faut préalablement s'y positionner par la commande 
**git checkout "nom_branche"**. On peut alors faire des modifications puis des commits par la commande classique **git commit -am "message"**.
pour fusionner  ces commits dans la branche master,il faut retourner dans cette branche puis utiliser la commande
**git merge 'autre branche que le master".

![]("C:/Users/skeita/Desktop/Branches/comit_branches_b1_merges_branches.PNG")


## Envoie d'une branche sur le serveur et vérification de sa présence sur la page web du serveur.
pour envoyer une branche autre que le master,créée en local ,on se positionne dans cette branche puis on uilise la commande
**git push --set-upstream origin "nom_branche"**

![]("C:/Users/skeita/Desktop/Branches/push_b1.PNG")


Il suffit d'utiliser la commande **git ls-remote** pour verfier si la branche pushée existe dans la liste des branches distantes.

![](""C:/Users/skeita/Desktop/Branches/verication_pushBranche.PNG")


## Création d'une nouvelle branche à partir du commit précédant dans le master courant et fusion dans le master de quelques commits réalisés dans la nouvelle branche . 
Il faudrait retourner au commit precédent du master(avant la fusion avec les modication d'une autre branche)par la commande 
**git checkout -- "adresse commit** puis créer la nouvelle branche dans le master (**git branch "nom_branche"**).Une fois des commits realisés dans la nouvelle branche sur des modifications faites, on peut utiliser la commande **git merge "nom_branche** dans le master.

![](""C:/Users/skeita/Desktop/Branches/b3_merge.PNG")

## Fusion  de la branche  master dans une autre branche et vérification du  graphe des commits avec le client Git console

![](""C:/Users/skeita/Desktop/Branches/larbre_commits_branches")
 

## Envoie d'une nouvelle branche  locale sur le serveur
pour envoyer une branche sur le serveur,on selectionne la branche puis on utilise la commande **git push --set-upstream "origin" "nom_branche"**
![]("C:/Users/skeita/Desktop/Branches/pushb3.PNG")

## Suppression d'une branche en à distance puis à locale
pour supprimer une branche,il est nécessaire de selectionner une autre branche (master de référence).On utilise les commandes **git branch -d "nom du branche "** pour la suppression locale et **git push --delete origin nom_branche"** pour la suppression à distance.

![]("C:/Users/skeita/Desktop/Branches/supression b3.PNG")

## Vérification du  graphe des commits avec le client graphique gitk

![]("C:/Users/skeita/Desktop/Branches/gitk.PNG")
Cette historique des commits faite après la suppresion d'une branche (b3),presente la liste listte des commits en indiquant les branches qui les contiennent.

![]("C:/Users/skeita/Desktop/Branches/fin.PNG")


