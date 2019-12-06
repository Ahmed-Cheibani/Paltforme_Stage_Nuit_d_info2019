# IsitcomBrightNight
Ce présent travail est réalisé dans le cadre du défi: Dockerisation (220) par les membres de l'équipe Bright_Night.

Les étapes de création d'un dockerfile :

# stage 1
FROM nginx:1.14.1-alpine   							   ** nous avons utilisé l'image nginx
COPY nginx/default.conf /etc/nginx/conf.d/             ** nous avons copier le config par défaut du nginx

COPY ./ /usr/share/nginx/html      						** nous avons copié le fichier du projet saharaDashboard dans nginx


Les étapes d'installation :
## Etape 1 :
Il faut cloner cette repository  qui présente l'image docker de notre application de plateforme des stages PFE.
Bien évidemment il faut déjà avoir le docker installé sur votre machine.


## Etape 2 :

Il faut taper cette commande  "docker build -t platfrom-stage ." sur le docker CLI afin de créer l'image à partir du Dockerfile.

## Etape 3 :
Il faut taper la commande suivante "docker run -p 8080:80 platfrom-stage" sur le docker CLI qui permet de faire l'exécution de l'image dans un conteneur docker.


## Etape 4 :

C'est la derniére étape qui consiste à affecter une adresse IP automatiquement au conteneur.

Et voilà le projet devient exécutable et prêt à être utilisé.# Dockerisation