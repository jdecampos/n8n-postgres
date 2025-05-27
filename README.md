# Installation de N8n avec PostgreSQL

## Préparation

1. Créer un dossier n8n

### Création du fichier .env

2. Ajouter un fichier `.env` et y mettre le contenu nécessaire
3. Modifier les informations nécessaires dans le fichier `.env`


### Création du fichier docker-compose.yml

4. Créer un fichier `docker-compose.yml` et y mettre le contenu nécessaire


## Création des volumes Docker


```bash
sudo docker volume create n8n_data
sudo docker volume create traefik_data
sudo docker volume create postgres_data
```
