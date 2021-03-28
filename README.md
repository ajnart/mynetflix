![](assets/mynetflix.png)

# Workshop MyNetflix part. 1

#### *Ce workshop a pour but d'automatiser le téléchargement des médias dès leurs sortie.*

### **N'hésitez pas à star ⭐ ce repo si vous avez aimé le workshop!** ![](https://img.shields.io/github/stars/ajnart/mynetflix-part1?label=%E2%AD%90&style=for-the-badge?branch=master&kill_cache=1")

Ce workshop est divisé en deux parties:  
1️⃣ La première concerne l'installation d'un conteneur Docker portainer; le déploiement d'un serveur de distribution de média Plex et le déploiement d'une interface de téléchargement de torrents grâce à transmission.

2️⃣ La seconde partie concerne la mise en place d'un "stack" via Dokcer-compose pour voir monter de dé-monter facilement tout nos conteneurs en une seule commande et l'installation de **sonarr/radarr/jackett** pour automatiser le téléchargement de nos médias.

## Partie 1 : Docker Compose
![](assets/docker-compose.jpg)

**Docker Compose** est un outil qui permet de décrire (dans un fichier YAML) et gérer (en ligne de commande) plusieurs conteneurs comme un ensemble de services inter-connectés.

Installez Compose si ce n'est pas déjà fait à l'aide du [tuto linuxserver](https://docs.linuxserver.io/general/docker-compose)
