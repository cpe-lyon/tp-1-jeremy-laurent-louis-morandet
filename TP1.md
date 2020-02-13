
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

## Commandes importantes

**QUESTION 1:** *Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?*
    
    date
    
Time permet d'afficher le temps d'execution 

**QUESTION 2:** *Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire sur les fichiers commençant par un point ?*

ls --> afficher les dossiers

la --> afficher les dossiers (cachés) quasi équivalent à:

    ls -a


**QUESTION 3:** *Où se situe le programme ls ?*

    which ls

**QUESTION 4:** *Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande.*

ll est un alias. Which ll ne renvoie rien
La commande alias permet de voir les alias configuré.

**QUESTION 5:** *Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?*

    ls -l /bin

**QUESTION 6:** *Que fait la commande ls .. ?*

Permet d'afficher le contenu du dossier parent

**QUESTION 7:** *Quelle commande donne le chemin complet du dossier courant ?*

    pwd

**QUESTION 8:** *Que fait la commande echo 'yo' > plop exécutée 2 fois ?*

créer un fichier nommée plop dont est: 
    
    yo

**QUESTION 9:** *Que fait la commande echo 'yo' >> plop exécutée 2 fois ?*

créer un fichier nommée plop dont est:
    
    yo
    yo


**QUESTION 10:** *A quoi sert la commande file ? Essayez la sur des fichiers de types différents.*

 Permet de donner le type de fichier

**QUESTION 11:** *Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi : qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?*

Permet de créer un lien vers le contenue du fichier (reference)

**QUESTION 12:** *Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle conséquence cela a-t-il sur tutu ?*

Permet de créer un raccourci vers le fichier

**QUESTION 13:** *Affichez à l’écran le fichier. Quels raccourcis clavier permettent d’interrompre et reprendre le défilement à l’écran ?*

    
    cat nomfichier
    
    CTRL + S --> stopper le défilement
    CTRL + Q --> reprendre le défilement
    
    CTRL + Z --> Mettre en pause un programme
    bg //redemare l'execution en arriere plan
    fg //remet le proggrame au premier plan


**QUESTION 14:** *Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les lignes 10 à 20.*

    head -n 5 /var/log/syslog  --> X première lignes
    sed -n '10,15p' /var/log/syslog --> intervale [X Y] lignes
    tail -n 15 /var/log/syslog --> X dernière lignes
    

**QUESTION 15:** *Que fait la commande dmesg | less ?*

Ce fichier contient l'ensemble des utilisateurs et leurs informations (mot de passe, numéro...). On utilise man 5 passwd pour afficher le manuel.


**QUESTION 16:** *Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page de manuel de ce fichier ?*

La commande 'dmesg|less' affiche la sortie de la premiere commande dans less qui permet l'affiche plus claire et lisible.

**QUESTION 17:** *Affichez seulement la première colonne triée par ordre alphabétique inverse*

    sort -d -r --> permet de trier par ordre alphabétique inversé.

**QUESTION 18:** *Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?*

     wc /etc/passwd --> affiche le nombre d'utilisateurs.

**QUESTION 19:** *Combien de pages de manuel comportent le mot-clé conversion dans leur description ?*

    man -k conversion | wc -l -> Permet d'afficher le nombre de page contenant la chaîne de caractère "conversion".

**QUESTION 20:** *A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine*

    sudo find / -name "passwd" | wc  -l --> Affiche le nombre de fichier dont le nom du fichier contient la chaine de caractère "passwd".
    
**QUESTION 21:** *Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier ~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null*

    find / -name 'passwd' > file.txt 2>/dev/null 

**QUESTION 22:** *Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu précédemment*

    cat .bashrc | grep ll

**QUESTION 23:** *Utilisez la commande locate pour trouver le fichier history.log.*

    locate history.log
    
Attention le package n'est pas installé de base

**QUESTION 24:** *Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?*

    locate -a testDeFichier (aucun résultats) 
    
Locate génère une sorte de base de donnée pour rechercher des fichiers... Il faut mettre à jours cette base de données manuellemenent pour que locate puisse trouver notre fichier. Il faut faire : 
    
    updatedb.

