
---
layout: post
title:  Base Secrete 2
date:   2020-06-04
---

#Base secrète 2:#

Commencez par télécharger le fichier getin2 utilisant *curl* et le lien du fichier. Stockez le dans un fichier en utilisant *-o leNomDuFichier* . Après il faut transformer ce fichier en éxécutable avec la commande *chmod u+x leNomDuFichier*. Puis il faut lancer le programme en strings pour pouvoir voir le code du programme, on fait cela en utilisant : *strings ./leNomDuFichier*. On va voir beacoup de ligne de code. La plupart ne nous intérèsent pas. Il faut trouver le mot de passe qui est définit comme une variable. On observe ça:

CrocodilH
esAreBigH
[]A\A]A^A_
=== This is a very secret base ===
Password:
 ACCESS GRANTED !!!
Use the password as the flag for the challenge
Access denied kid!!

 **CrocodilesAreBig** est la variable qu'on cherche.  Cette variable est donc le mot de passe et le flag qu'on veut trover.​​​