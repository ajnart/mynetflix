![](assets/mynetflix.png)

# Workshop MyNetflix part. 1

#### *Ce workshop a pour but d'automatiser le téléchargement des médias dès leurs sortie.*

### **N'hésitez pas à star ⭐ ce repo si vous avez aimé le workshop!** ![](https://img.shields.io/github/stars/ajnart/mynetflix-part2?label=%E2%AD%90&style=for-the-badge?branch=master&kill_cache=1")

Ce workshop est divisé en deux parties:  
1️⃣ La première concerne l'installation d'un conteneur Docker portainer; le déploiement d'un serveur de distribution de média Plex et le déploiement d'une interface de téléchargement de torrents grâce à transmission.

2️⃣ La seconde partie concerne la mise en place d'un "stack" via Dokcer-compose pour voir monter de dé-monter facilement tout nos conteneurs en une seule commande et l'installation de **sonarr/radarr/jackett** pour automatiser le téléchargement de nos médias.

### Cleanup
⚠ Vous devez d'abord supprimer les conteneurs que vous avez créer durant l'étape précédente. Sinon docker ne pourra pas attribuer les ports nécessaires aux bons services 

## Partie 1 : Docker Compose
![](assets/docker-compose.jpg)

**Docker Compose** est un outil qui permet de décrire (dans un fichier YAML) et gérer (en ligne de commande) plusieurs conteneurs comme un ensemble de services inter-connectés.

Installez Compose si ce n'est pas déjà fait à l'aide du [tuto linuxserver](https://docs.linuxserver.io/general/docker-compose)

Vous pouvez maintenant télécharger les images que nous allons utiliser à l'aide de ``docker-compose pull``

### Partie 2 : Configuration de docker compose
Comme vous pouvez le voir dans le fichier ``docker-compose.yml`` mis à votre disposition dans dans le repo, il manque des paramètres pour permettre l'execution des conteneurs.

Pour corriger ça, mettez en place la configration recommandée grâce aux liens suivants:

| service      | Lien |
|--------------|------|
| plex         | [linuxserver/plex](https://docs.linuxserver.io/images/docker-plex)
| transmission | [linuxserver/transmission](https://docs.linuxserver.io/images/docker-transmission)
| radarr       | [linuxserver/radarr](https://docs.linuxserver.io/images/docker-radarr)  
| sonarr       | [linuxserver/sonarr](https://docs.linuxserver.io/images/docker-sonarr)
| jackett      | [linuxserver/jackett](https://docs.linuxserver.io/images/docker-jackett)

**Faites attention à bien rensigner des chemins / volumes valides.**

![](assets/carbon.png)

Une fois que tout les services sont mis en place, vous pouvez lancer la stack grâce à ``docker-compose up``

