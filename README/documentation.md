# Documentation
Commencons par décortiquer chaque nouvelles notions vus dans le sujet ^^'

## Sommaire
- Docker
- Conteneurs
- Docker image
- Docker compose


## Docker
Plateforme de conteneurisation qui permet d'empaqueter des applications et leur dépendances dans un conteneur déployable dans n'importe quel environnement.


## Conteneur
Les plateformes de conteneurisation permettent d'empaqueter des aplications pouvant être déployées 
sur differents systèmes en regroupant le code logiciel, les bibliothèques ainsi que toutes les dépendances nécessaires pour éxecuter le code en formant un seul executable nommé **conteneur**

Utiliser une plateforme de conteneurisation pour le developpement d'applications 
permet aux équipes de développeurs de déployer les applications rapidement.
Les conteneurs se reposent sur l'os du système hôte en partageant ses ressources plutot que d'en associer un nouvau par application comme avec les machines virtuelles, ce qui les rends plus légers et reduit lse couts de serveurs et licenses.

Les fichiers nécessaires a l'execution du conteneur sont fournis par une image distincte


## Image Docker
Fichier executable qui contiennent toutes les instructions, pour executer un conteneur. Il contient toutes les bibliothèques dépendances et fichiers
dont le conteneur aura besoint pour s'executer.
Lorsqu'une image docker est executué, elle devient une instance du conteneur.

Les images sont immuables une fois crées elles ne peuvent etre modifié.
Cependant elles sont composé de couches d'images en lecture seule représentant chacune les modifications apportées à l'image.

les images docker permettent donc de stocker les details de configuration de l'application.


## Docker Compose
Docker Compose est un outil permettant de configurer et executer tous les  conteneurs dont l'application aurait besoin dans un fichier de configuration YAML.


## Alpine et Debian
Alpine: Distribution linux très légère et minimaliste, 
son image ISO pèse entre 46Mo (virtuel) et 627Mo  selon les versions
et occupe entre 106Mo(virt) et 1,1Go (standard).
Alpine est populaire pour son niveau de sécurité, 
la création d'image conteneurs, les systèmes embarqués 
et machines virtuelle. 

Debian: distribution linux libre, nouvelles versions toujours stables
adaptées aux vieux pc car pas très gourmads en ressources (en comparaison a ubuntu)



## Sources utiles
https://www.ibm.com/fr-fr/think/topics/docker
https://www.ibm.com/fr-fr/think/topics/containerization
https://www.docker.com/resources/what-container/
https://www.redhat.com/fr/topics/containers/un-conteneur-linux-quest-ce-que-cest
https://aws.amazon.com/fr/compare/the-difference-between-docker-images-and-containers/
https://www.nicelydev.com/docker

[left][👈 Page précédente](../README.md)[/left][right]Démarrons [👉](./documentation.md){.btn .btn-lt}[/right]
