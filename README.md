# Presentation NPM

## Qu'est ce qu'NPM (Ou Node Package Manager)

Npm est un gestionnaire de paquet, il permet de partager des packages avec n'importe qui utilisant aussi NPM, vous pouvez aussi gerer des paquets prives.
Npm se divise en 3 grands axes :

## Le site

Le site [NPM](https://www.npmjs.com/) est utile pour connaitre les packages disponibles au telechargement depuis le Registry NPM (Voir plus bas)

## L'interface en ligne de commande

L'interface en ligne de commande est utilisee par la majeure partie des developpeurs, avec l'interface en ligne
de commande vous etes apte a telecharger des packages, telecharger des applications depuis le Registry NPM.
Vous pouvez telecharger des packages et les adapter a vos besoins.
Vous pouvez aussi executer des packages depuis le Registry sans avoir a les telecharger

## Registry ou L'enregistreur

Le Registry NPM n'est ni plus ni moins qu'une enorme base de donnees de packages JS pouvant aussi contenir des applications
Accessible partout en utilisant NPM

## Pourquoi utiliser NPM

Utiliser NPM c'est developper avec tous les developpeurs qui l'utilisent aussi; Vous pouvez partager des packages avec eux 
mais aussi recuperer des packages de leur part. Pourquoi recreer ce qu'un autre a deja cree, surtout en prennant en compte le fait
qu'il est possible d'adapter les packages a vos besoins comme explique ci dessus.
Vous pouvez trouver d'autre developpeurs qui ont les memes problemes que vous, ou les memes projets. Et par dessus tout, trouver d'autres moyens de patcher des problemes que vous rencontrez ou avez rencontre. Trouver d'autre moyen de developper de nouvelles fonctionnalites

## Qu'est ce qu'NPX (Node Package Execute)

NPX est un module de NPM, il vous permet d'executer une application depuis le Registry NPM sans avoir a le telecharger au prealable

## Comment installer NPM ?

Pour installer NPM c'est assez simple 

```
sudo apt-get install nodejs
```

Ou

```
pacmam -S nodejs
```

Une fois Node installe, installez NPM

```
sudo apt-get install npm
```

Ou

```
pacmam -S npm
```
<br>

# NPM Presentation

## What is NPM (Node Package Manager)

Npm is a large software to manage packages, with everybody else, you can also use npm to manage private packages
Npm is devided by 3 large axes :

## The Website

[NPM](https://www.npmjs.com/) Website is usefull to know which packages are availables on NPM registry (See below)

## The Command Line Interface (Or CLI)

CLI's used by the major part of developpers, with the CLI you're able to download packages.
Download some software on registry, to run them.
You can download some packages and adapt them to your needs too.
You're able to run packages without downloading them (Using NPX).

## The Registry

The registry is just a large database of JavaScript tools and packages
Accessible from everywhere using NPM

## Why use NPM

Using NPM is developping with all developpers on, you can share your packages with them and get
some packages of them, why create something that somebody else already created, mostly if you can adapt
downloaded packages at your needs like explained above ? 
Yun can find other developpers who have same problems or projects. And above all you can find diffents ways to fix a problem,
searching another way to create a feature.

## What is NPX (Node Package Execute)

NPX is an module of NPM who'll able you to execute packages without downloading them, if package is in NPM registry
you'll be able to run it

## How to Install ?

NPM is pretty easy to install

```
sudo apt-get install nodejs
```

Or

```
pacmam -S nodejs
```

Then, install npm

```
sudo apt-get install npm
```

Or

```
pacmam -S npm
```



# Les commandes NPM

### Comment initialiser un projet avec NPM ?

> **npm init**

Le npm init va cr??er un fichier **package.json** qui va permettre d'obtenir des informations sur son projet.

### Comment installer des modules ?

- ##### Pour pouvoir ajouter un nouveau pacquet ?? son projet il faudra utiliser :

##### Exemple :

> **npm install express**
OR 
> **npm i express**

 

- ##### Pour pouvoir installer les pacquet d??j?? existants il faudra utiliser :

> **npm install**
OR
**npm i**

Cette commande va permettre d'installer tous les pacquet et modules qui ont ??t?? ajout??es au projet dans le fichier **package.json**.

- ##### Vous pouvez t??l??charger une version sp??cifique d'un package pour revenir ?? une version ant??rieur, il vous faudra donc utiliser :

##### Exemple :

> **npm install express@1.0.2**

### Comment installer les pacquet de d??pendance de d??veloppement ?

- ##### Pour installer les outils qui ne seront utilis??s que dans l???environnement de d??veloppement, il faudra utiliser :

##### Exemple : 

> **npm install nodemon --save-dev**

Il y aura donc dans le fichier **package.json** le **devDepencies** qui va ??tre ajouter.

### Comment list??s des packages install??s au projet ?

- Pour lister les packages, au niveau local, il faudra utiliser la commande : 
> **npm list**

OR

> **npm ls**

### Obtenir des informations sur un package

- Pour avoir des informations sur un package, il faudra utiliser :
> npm **view express**

- Pour avoir de la documentation sur le package, il faudra utiliser :
> npm **docs express**

### Quels sont les commandes pour faire les mises ?? jours de NPM ?

**IMPORTANT** : Il faut toujours v??rifier que les modules et paquets sont ?? jours.

- ##### Que faire avant de mettre ?? jour un paquet NPM ?

- Avant de mettre ?? jour **les paquets NPM** il faut regarder si un paquet est expir??, il faudra utiliser : 

> npm **outdated**

Il faudra utilis?? la commande depuis le r??pertoire racine.

#### Il y a deux type d'update :

- Pour mettre ?? jour tous les paquets du projet, il faudra utiliser :

> npm **update**

- Pour mettre ?? jour un paquet en particulier, il faudra utiliser : 

> npm **update express**

#### Mettre ?? jour la nouvelle version NPM :
- Pour mettre ?? jour la nouvelle version de NPM, il faudra utiliser : 
> npm **install npm@latest -g**

#### Mettre ?? jour les packages de d??veloppement :
- Pour mettre ?? jour un package en DevDepencies, il faudra utiliser :
> npm **update --dev**

### Quels sont les commandes pour d??sinstaller un package ?

- Pour supprimer un package en local, il faudra utiliser la commande :

> npm **uninstall express**

OR
> npm **un express**

- Pour supprimer les packages du cache, il faudra utiliser la commande : 
> npm cache clean

## Utilisation de script NPM

##### Comment executer un script ?

- Pour permettre d'??xecuter un script et le faire fonctionner, il faudra utiliser :

> npm **run nodemon**

OR

> npm **run-script nodemon**

#### Comment voir la liste des scripts ?

- Pour pouvoir voir la liste des scripts ?? disponible, il faudra utiliser la commande :

> npm run

#### Quels sont les autres commandes ?

- Certaines actions peuvent ??tre ex??cut??es directement sans forc??ment utiliser la commandes :

> npm run **start.js**

- ##### Quels sont les autres actions ?

- Pour produire un fichier compress?? des fichiers ?? d??ployer, il faudra utiliser :

> npm **pack**

- Pour publier un package, il faudra utiliser :

> npm **pulish**

- Pour ex??cuter le script **start** qui sert g??n??ralement pour stopper le serveur Node.js, il faudra utiliser :

>npm **start**

- Pour ex??cuter le script **stop** qui sert g??n??ralement pour stopper le serveur Node.js, il faudra utiliser :

>npm **stop**

- Le script **restart** va ex??cut?? les scripts **stop** et **start**, il faudra donc utiliser la commande : 

> npm **restart**

- Pour supprimer un package qui a ??t?? publi??, il faudra utiliser : 

> npm **unpublish**
