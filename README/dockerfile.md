## Dockerfile

Dockerfile est un fichier permettant de creer une image docker a partir d'une suite d'instructions qui installe toutes les edépendances nécessaire pour l'application a partir d'une image de base.

A chaque instruction, docker crée un conteneur temporaire execute l'instruction,
capture la différence des fichiers puis la stock comme une nouvelle couche.

### Syntaxe

Un dockerfile doit toujours commencer avec l'instruction FROM, qui va définir l'image de base.

*FROM [--platform]<platform> <image>[:<tag>] [AS <name>]
 FROM debian 
 FROM debian:bullseye*
 