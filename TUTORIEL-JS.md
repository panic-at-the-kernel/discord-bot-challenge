# **Comment tester votre bot**

## Summary

1. [Installation de Node JS](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#1installation-de-node-js)

    a. [sur Windows](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#asur-windows)   
    b. [sur Linux](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#bsur-linux)  
    c. [sur macOS](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#csur-macos)  

2. [npm & discord.js](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#2npm--discordjs)

3. [Comment créer un bot discord](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#3cr%C3%A9er-un-bot-discord)

4. [Comment tester votre bot](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#4comment-tester-votre-bot)

5. [Liens utiles](https://github.com/panic-at-the-kernel/discord-bot-challenge/blob/main/TUTORIEL.md#5liens-utiles)

## 1. Installation de Node JS

### a. sur Windows

Vous pouvez vous rendre sur cette page, pour télécharger un installeur correspondant à votre système d'exploitation <https://nodejs.org/en/download/>.

### b. sur Linux

Il y a toujours moyen de télécharger des installeurs <https://nodejs.org/en/download/>, sauf si vous utilisez wsl. Mais dans le cas ou vous utilisez wsl ou que vous vouliez montrer votre cool maîtrise du terminal, on peut l'installer grâce à vos packages manager. Une explication est détaillé sur ce lien <https://nodejs.org/en/download/package-manager/>, mais nous allons couvrir les packages manager des distro linux (ou wsl) manquant ou complexe ici :

Ubuntu (je vous ai dis que c'était simple bah pour celui-là c'est pas tout à fait vrai, mais ça se digère ne vous inquiètez pas) :

1. Ouvrez votre terminal.

2. ```cd ~``` juste pour être certains d'etre dans votre home directory.

3. ```curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh``` avec ça vous allez télécharger un script pour setup le bon package provider, parce que bah celui de base vous donnerait une version qui n'est pas comptatible avec discord... allez savoir pourquoi ¯\_(ツ)_/¯.

4. ```nano nodesource_setup.sh``` une bonne pratice à faire plus souvent, lire le script essayer d'avoir une compréhension basique de ce qu'il ait avant de le run.

5. Une fois satisfait quitter nano (ou tout autre éditeur utilisé) que l'on puisse reprendre. PS : si vous êtes coincé dans nano ne paniquez pas c'est moins horrible que vim un petit ```Ctrl+x``` fera l'affaire.

6. ```sudo bash nodesource_setup.sh``` on lance le script avec un petit sudo. ça indexera le nouveau magasin de package.

7. ```sudo apt install nodejs``` installera nodejs.

8. ```node -v``` vous renverra un numéro de version installé, si la version est supérieur à 14 on peut s'y mettre.

### c. sur macOS

C'est un peu comme linux au fond, vous pouvez aller chercher un exécutable ici <https://nodejs.org/en/download/>, sinon brew fera super bien l'affaire avec un simple ```brew install node```.

## 2. npm & discord.js

Pour cela, il nous faut deux pièces principales npm, qui est le package manager de node js, et un package de node.js appelé discord.js.

Si vous avez installé node avec un exécutable npm est bundled avec donc vous êtes quasi bon :

* Vérifions que npm est bien installé avec ```npm version```

* Assurons nous maintenant d'avoir la dernière version de npm, en effet ils ont beau être packager ensemble, leur rythme de dévelopement est asynchrone. ```npm install npm@latest -g``` permettra à npm de se mettre à jour.

Si vous avez installé node.js avec un package manager, il vous suffit normalement de transposer la même commande par exemple pour ubuntu (et autre ubuntu based distro):

* ```sudo apt install npm``` pour installer.

* ```npm version``` pour vérifier que c'est bon.

* ```npm install npm@latest -g``` pour s'assuer d'avoir la dernière version.

Si vous avez tenu jusque là plus qu'une petite étape pour que votre environnement de dev soit opérationnel, ```npm i discord.js``` et on est bon, happy programming.
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
.  
C'est bon ? parfait, maintenant allons jeter un oeil sur comment tester cette nouvelle fonctionnalité en créant un moyen de tester ce code en condition réelle.

## 3. Créer un bot discord

1. Pour tester votre code il va falloir créer un bot permettant de tester les nouveaux features, pour cela il suffit de se rendre sur ce portail <https://discord.com/developers/applications/me>, de ce log si cela vous est demandé.

2. En haut à droite vous verrez un bouton ```New Application```, précisez un nom, de préférence assez représentatif de la fonction de votre application.

3. Ensuite rentrez dans votre application sous le menu bot, vous devriez voir build-a-bot, avec un bouton create, il est possible que le nom soit trop courant (apparemment testbot était déjà trop courant aller savoir pourquoi) dans cas la il vous faut modifier le nom en ajoutant par exemple des chiffres (testbot1 for the win)

## 4. Comment tester votre bot

1. Créer un serveur discord pour tester votre bot.

2. Lancer le bot avec node.

3. L'inviter avec l'outil sur le portail développeur discord, sous le panel OAuth2, sélectionner bot dans les scopes, puis avec les permissions adaptées.

4. Copier coller l'url que cela génère dans la barre url de votre navigateur, et ajouter le à votre serveur de test.

5. Vérifier que les commandes fonctionnent dans un channel.

## 5. Liens utiles

<https://nodejs.org/en/download/>  
<https://discord.com/developers/applications>  
<https://www.grafikart.fr/tutoriels/bot-discordjs-892>  
<https://www.grafikart.fr/tutoriels/nodejs>  

PS : Si il vous reste une question, n'hésitez pas à nous contacter @kernel panic sur le serveur discord licence informatique@uca
