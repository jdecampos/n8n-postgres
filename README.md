# Installation de N8n avec PostgreSQL

## Préparation

1. Créer un dossier n8n `mkdir n8n`
2. Aller dans le dossier `cd n8n`

### Création du fichier .env

3. Ajouter un fichier `nano .env` et y mettre le contenu nécessaire
4. Modifier les informations nécessaires dans le fichier `.env`


### Création du fichier docker-compose.yml

5. Créer un fichier `nano docker-compose.yml` et y mettre le contenu nécessaire

## Installer Docker 

# 1. Mettre à jour les packages
```bash
sudo apt update
```

# 2. Installer les dépendances nécessaires
```bash
sudo apt install -y ca-certificates curl gnupg lsb-release
```

# 3. Ajouter la clé GPG officielle de Docker
```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

# 4. Ajouter le dépôt Docker
```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

# 5. Installer Docker
```bash
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Installer Docker compose 

```bash
sudo apt-get update
sudo apt-get install docker-compose-plugin
```

## Création des volumes Docker

6. Copier ces lignes de commande

```bash
sudo docker volume create n8n_data
sudo docker volume create traefik_data
sudo docker volume create postgres_data
```
