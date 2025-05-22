# Documentation
Commencons par décortiquer chaque nouvelles notions vus dans le sujet ^^'

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


## NGINX (Prononcé engine-x ☝️🤓)
NGINX est un logiciel gratuit et open source écrit par Igor Sysoev en 2004. 
Au départ concu pour répondre au problème de limitation des serveurs sur de tres grands nombres de connexions simultanées, nginx aujourd'hui répond à une multitude de besoins tels que :
	- serveur proxy inverse => serveur intermediaire entre le client et le(s) serveru web
	- load balancing => optimise les ressources et le temps de réponse en distribuant le trafic réseau sur plusieurs serveurs
	- Caching HTTP => stockage des reponses associé a des requetes localement afin de reutiliser la reponse stocké afin d'améliorer le temps de réponse 
	- suppor ssl et tls => communication sécurisées client/serveur

	*TLSv1.2/v1.3*:  Le TLS Transport Layer Securituy est un protocole de sécurité concu pour la confidentialité et la sécurité des données sur les communications internet ainsi que le chiffrement d'autres communications (mails, messagerie..). Dans notre contexte, TLS permet aux communications sur Internet d'être privée et sécuriséesht. Voir un https et/ou un cadenas visible au debut de l'url nous informe que la connexion utilise TLS.

## MariaDB
Système de gestion de base de données relationnelle (SGBDR) gratuit et open source lancé en 2009 par le fondateur de MySQL Michael Widenius  après le rachat de cette dernière par Oracle Corp.

## WordPress
Système de gestion de contenu (CMS) gratuit et aussi open source. 
WordPresse a pour fonctionnalité de créer et gérer differents types de site web (blog, site vitrine, vente en ligne) sans pour autant savoir coder.

#PHP-FPM (FastProcessManager)
Gestionnaire de processus FastCGI (protocole de communication permettant NGINX a communiquer avec des applications) pour executer du php sur un serveur web
qui permet d'améliorer les performances et la gestion du processus PHP sur des serveurs à fort trafic. Le serveur web envoie les requetes PHP à PHP-FPM qui les exécute en crèant un pool de processus PHP pour eviter de lancer un ouveau processus PHP pour chaque requête.

# PID 1 (Process IDentifier)
A chaque démarrage d'un nouveau processus est attribué un code unique permettant d'identifier le processus.

Sous linux le premier programme lancé par le noyeau se voit attribuer le PID 1 après l'initialisation du système, ce PID 1 est responsable des séquences d'arret redemarrage et changement d'état du système.

Dans un conteneur docker, le processus démarré devient le PID 1 à l'interieur du conteneur et a des responsabilités similaires a *init*.

si le rôle de PID n'est pas bien gérer (signaux non géré, mauvais gestion de l'application) des fuites ou un crash peut arriver.

## Sources utiles
https://www.ibm.com/fr-fr/think/topics/docker
https://www.ibm.com/fr-fr/think/topics/containerization
https://www.docker.com/resources/what-container/
https://www.redhat.com/fr/topics/containers/un-conteneur-linux-quest-ce-que-cest
https://aws.amazon.com/fr/compare/the-difference-between-docker-images-and-containers/
https://www.nicelydev.com/docker

[👈 Page précédente](../README.md)

[Démarrons 👉](./demarrage.md)
