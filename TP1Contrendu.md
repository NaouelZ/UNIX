*Naouel Zenati* 

*Projet Web et Mobile*

# 			 TP 01  : Installation Serveur

## I- Installation de la machine virtuelle

Dans un première temps il a fallu créer la machine virtuelle. Nous avons pour cela utilise le système de machine virtuel **VirtualBox** avec la *distribution Linux Debian* et de type *amd64*.

### 	I.1 - Debian et support d'installation

​	Pour l' installation de notre Debian _"stable"_, nous avons besoin d'une image iso.  Nous allons utilisé l'image suivante :  **mini.iso**. Celle-ci contient le strict minimum requis pour configurer le réseau, tout le reste est télécharger lors de l’installation.

### 	I.2 - Récupération de l'installeur

​	Il a fallu se rendre dans l'url suivante : 

[Debian]: ftp.lip6.fr/pub/linux/distributions/debian/

Ensuite pour l'image **mini.iso** se trouvais dans le chemin suivant:

url-mirroir/dists/stable/main/installer-md64/current/images/netboot/

### 	I.3 - Création de la machine virtuelle

Pour la création de la machine, j'ai suivi les étapes cité dans le sujet du TP.

En effet, tout d'abord j'ai lancé le logiciel __VirtualBox__. Ensuite j'ai crée une nouvelle machine en cliquant sur _"Nouvelle"_. Ensuite, j'ai nommée celle-ci _"serveur1"_, de type _"Linux"_ et la version _"Debian (64-bits)"_ comme demandé dans le sujet. J'ai choisi une RAM de 512Mo, et, crée un disque dur d'amorçage allouée _dynamiquement_, de taille _10Go_ et de type _"VDI"_. Ensuite, j'ai importé l'image **mini.iso**, *( voir 1.1)* , en cliquant sur _"Configuration"_, puis sur _"Stockage"_ etc..

Puis j'ai lancer la machine en cliquant sur le bouton _Démarrer_ .

### 	I.4 - Installation

J'ai ensuite lancer _"



## II - Post-Installation 

### 	II.1 -  Configuration SSH

On se connecte tout d'abord en root avec la commande  :

```
sudo -
```

   Ensuite, on installe SSH avec la commande : 

```
apt install ssh
```

On vérifie si cela a bien été installé :

```
apt search ssh
```

Pour pouvoir changer la connexion root à distance avec mot de passe, il faut :

```



```

### 	II.2 - Connection

Pour se connecter, nous avons utilisé l'utilitaire _cmder+_. Dans un premier temps , je l'ai installé.

Avant de pinger les machines, il a fallu qu'on se mette soit en réseau interne soit en bridge.  Dans mon cas, je suis resté en bridge _( Accès par pont)_.  

J'ai dans un 1er temps pinger du _"client"_ vers le server1.

```
ping 127.0.0.1
```

Ensuite,  sur notre serveur1, il a fallu pinger du serveur au client. Pour retrouver, l'adresse IP de celui-ci. J'ai utilisé la commande suivante :

```
ip a
```

J'ai ensuite pinger sur celui-ci 

```
ping 134.157.46.189
```

### 	II.3 - Nombre de paquets

​	Nous devions ensuite vérifié la taille de notre paquet soit bien inférieur à 239 paquets pour cela nous avons utilisé la commande suivante :

```
dpkg -l | wc -l
```

J'ai donc obtenue le résultat suivant :

