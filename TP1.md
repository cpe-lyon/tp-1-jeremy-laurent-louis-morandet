
# TP 1 : (LAURENT - MORANDET)
## Exercice 2
### MANUEL
**QUESTION 1:** *A l’aide du manuel, identifiez le rôle de la commande which?*
which  renvoie le chemin des fichiers (ou liens) qui seraient exécutés dans l'envi‐
ronnement courant si ses arguments avaient été donnés comme commandes dans  un  in‐
terpréteur  de commandes strictement conforme à POSIX. Pour ce faire, which cherche
dans la variable PATH les fichiers exécutables correspondant  aux  noms  des  argu‐
ments. which ne normalise pas les chemins.

**QUESTION 2:** *Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercherle terme option dans la page de manuel de which ?*
Pour les recherches manuels dans MAN, utilisez la touche "/"

**QUESTION 3:** *Comment quitte-t-on le manuel ?*
Pour quittez le MAN, pressez la touche Q

**QUESTION 4:** *Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la première page de la section 6 ; de quoi parle cette section ?*
Chaque section du manuel à un page d'intro: pour afficher la section 6, tapez: man 6 intro

## Navigation dans l'arborescence des fichiers
**QUESTION 1:** *allez dans le dossier /var/log*
cd /var/log

**QUESTION 2:** *remontez dans le dossier parent (/var) en utilisant un chemin relatif*
cd ..

**QUESTION 3:** *retournez dans le dossier personnel*
cd

**QUESTION 4:** *revenez au dossier précédent (/var) sans utiliser de chemin*
cd -

**QUESTION 5:** *essayez d’accéder au dossier /root ; que se passe-t-il ?*
-bash: cd: /root: Permission denied

**QUESTION 6:** *essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez*
On peut y acceder, sudo permet d'avoir les privilège super utilisateur.

**QUESTION 7:** *à partir de votre dossier personnel, créez l’arborescence suivante :*
mkdir Dossier1 Dossier2
touch Dossier1/Fichier1
mkdir Dossier2/Dossier2.1 Dossier2/Dossier2.2
touch Dossier2/Dossier2.2/Fichier2 Dossier2/Dossier2.2/Fichier3


**QUESTION 8:** *revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1 ; que se passe-t-il ?*
rm Dossier1/Fichier1
rm Dossier1
rm: cannot remove 'Dossier1': Is a directory

**QUESTION 9:** *quelle commande permet de supprimer un dossier ?*
rmdir Dossier1

**QUESTION 10:** *que se passe-t-il quand on applique cette commande à Dossier2 ?*
rmdir Dossier2/
rmdir: failed to remove 'Dossier2/': Directory not empty


**QUESTION 11:** *comment supprimer en une seule commande Dossier2 et son contenu ?*
rm -R Dossier2
