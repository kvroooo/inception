## Dockerfile

Dockerfile est un fichier permettant de creer une image docker a partir d'une suite d'instructions qui installe toutes les edépendances nécessaire pour l'application a partir d'une image de base.

A chaque instruction, docker crée un conteneur temporaire execute l'instruction,
capture la différence des fichiers puis la stock comme une nouvelle couche.

### Syntaxe

Un dockerfile doit toujours commencer avec l'instruction **FROM**, qui va définir l'image de base.

```
FROM [--platform]<platform> <image>[:<tag>] [AS <name>]
FROM debian:bullseye 
 ```
le paramètre [:tag] permet de spécifier la version de <image>, ce tag est optionnel cela dit s'il n'est pas appliqué Docker utilisera latest par défaut
ce qui pourrait apporter des problèmes de compatibilité avec notre container.

**RUN** lance des commandes à la construction de l'image, cette commande permet aussi d'installer des packages depuis notre image de base.
On pourrait appeler RUN pour chaque commande cependant comme a chaque instruction RUN ajoute une nouvelle couche à l'image, cela augmenterait la taille de l'image.
Pour palier a ca il est conseiller d'appeler les commandes en les separants par *&&* (pour debug, utiliser plusieurs *RUN* sera par contre plus utile)

```RUN apt update && apt install git```

Si les commandes sont trop longues, le caractère antislash permet de poursuivre l'instruction en allant a la ligne

```RUN apt update &&\
apt install nignx 
``` 

**COPY**: permet d'ajouter des fichier et dossiers pour les ajouter dans le systeme de fichier de l'image

**VOLUME**: crée un mountpoint a partir d'un hôte ou d áutres conteneurs,
ce aui permet de stokcer des données qui persistent meme lorsque le conteneur est arrêter voir meme supprimé.

**EXPOSE**: informe Docker que le conteneur écoute sur les ports réseau au moment de l'execution, il est possible de spécifier le protocole TCP/UDP, TCP est la valeur par défaut si aucun protocole n'est donné.


**CMD** et **ENTRYPOINT** : donnent la commande à executer au demarrage de l'image container, il ne peut y avoir qu'une instruction **CMD** dans un dockerfile. **ENTRYPOINT** definit la commande principale qui sera toujours executée au démarrage du conteneur, clest le processus principale qui me peut pas etre facilement remplacé. A la différence de **CMD** qui fournit les parametres par defaut a l'entrypoint ou alors la commande 

## Commandes container docker

**docker build [opt] <PATH>**: permet de construire le conteneur a partir du dockerfile
	docker build -t [name] <path> attribue un nom a notre image

**docker image ls**: liste les images deja build 

**docker run [opt] <img_name>**: demarre une image 
	[-it]: nous donne accées au aterminal du container au démarrage

**docker [opt] ps**: liste les containers actuellement lancés