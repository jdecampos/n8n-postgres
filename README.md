# Installation de N8n avec PostgreSQL

## Préparation

1. Créer un dossier n8n `mkdir n8n`
2. Aller dans le dossier `cd n8n`

### Création du fichier .env

3. Ajouter un fichier `nano .env` et y mettre le contenu nécessaire
4. Modifier les informations nécessaires dans le fichier `.env`


### Création du fichier docker-compose.yml

5. Créer un fichier `nano docker-compose.yml` et y mettre le contenu nécessaire


## Création des volumes Docker

6. Copier ces lignes de commande

```bash
sudo docker volume create n8n_data
sudo docker volume create traefik_data
sudo docker volume create postgres_data
```
