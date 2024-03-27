# test en local

Le test local repose sur une image docker qui package un nginx et pousse les répertoires qu'il faut.

Si on ajoute un répertoire correspondant à une nouvelle personne il faut modifier le fichier Dockerfile.

Pour faire le build
```shell
docker build -t declicimmo .
````

Et ensuite on peut lancer l'image

```shell
docker run -p 80:80 declicimmo
```

# déploiement sur le serveur declicimmo

Le plus simple est de se connecter en ssh sur la machine pour créer les répertoires nécessaires.

```shell
scp -P 38853 declicimmo@2.15.249.172
````

Ensuite on pousse les fichiers en indiquant le chemin cible complet.

Exemple, ici on pousse photo.jpeg dans le path complet dans le répertoire lié à Christophe

```shell
scp -P 38853 photo.jpeg declicimmo@2.15.249.172:/home/declicimmo/www/html/christophe/photo.jpeg
```