CONFIGURER GIT

git --version : vérifier la version de git et si Git est sur notre pc 
git config --global user.name "Your Name" :  définir notre nom 
git config --global user.email "youremail@example.com" : configurer email

CREER DEPOT 

mkdir <FOLDERNAME> : créer un nouveau dossier
cd <FOLDERNAME> : entrer dans le dossier
git init : dire à Git d'initialiser(démarrer le suivi) du dossier dans lequel on est. L'activer pour un repertoire
ls : Lister les éléments dans un dossier

COMMITS


Ouvrir éditeur de texte et créer un fichier txt ou md

git status : verifier le statut
git add readme.txt : ajoute le fichier que vous venez de créer afin qu'il devienne une partie des modifications que vous soumettez avec   Git
git commit -m "Création du fichier readme" : soumettez (commit) ces modifications à l'historique du dépôt avec un court (m) message décrivant les mises à jour.
git diff : suite à ajout de ligne dans le fichier,  affiche les différences entre le fichier actuel et la dernière version soumise.


AJOUTER NOM UTILISATEUR GITHUB A GIT

git config --global user.username <USerNamE> : Ajoute votre nom d'utilisateur GitHub à votre configuration Git
git config --global user.username : vérifier ce qu'on a configuré dans Git


REMOTE 

Aller à github.com , connectez-vous, puis cliquez sur '+' dans le haut À droite, puis cliquez sur 'New repository'.
Donnez-lui un nom qui correspond au nom de votre dépôt local, 'hello-world'
Rendez-le public
Ne pas initialiser avec un README car nous avons déjà un fichier, localement, nommé "readme.txt".
Laissez «.gitignore» et «licence» définis sur «none».

Connexion depot local au remote

git remote add origin <URLFROMGITHUB>:ajoute une télécommande nommée 'origine' à votre dépôt

Pousser travail dans le remote

git push origin master : Envoi notre branche nommée 'master' à notre remote sur GitHub nommée 'origin'.




git checkout : changer de branche et de revenir en arrière

git checkout -b « nom » : créé branche et switch

git switch : changement de branche

git switch main : switch de branche vers main

git branch « nom » : créé nouvelle branche


git merge :

git branch -D « nom » : supprime la branche


créé .gitignore ( dedans mettre ce qu’on veux ignorer)
add et commit


LIVRABLE EXO 7 

Un conflit arrive quand par exemple 2 personnes travaille sur le même fichier chacun en local et qu'ils veulent push sur GitHub. Cela créé un conflit, on nous propose donc doit d'ecraser une partie, soit de garder les 2.

Il faut git pull, notre editeur de texte s'ouvre avec le message de conflit de fusion. Il faut supprimer les marqueurs <<<<<<<< ========= >>>>>>>> puis $ git add. puis refaire un commit avec un commentaire comme "Resolved merge conflict"
Et on peut push après cela.