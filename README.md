
# Déploiement d'un cluster Hadoop

Déploiement d'un cluster Hadoop sur docker.

Ce cluster est composé d'un namenode et de trois datanode.


## Prérequis

- Git

- Docker Engine

- Docker Compose


## 🛠 Configuration



Cloner le repository

```bash
git clone https://github.com/baha1218/HadoopCluster.git
```

Rendez-vous dans le dossier HadoopCluster/ pour builder votre image

```bash
cd HadoopCluster/
docker build -t hadoop-spark .
```

Vous pouvez maintenant déployer vos 3 conteneurs grace au fichier `docker-compose.yml`. Utilisez `docker-compose` si vous n'etes pas sur red hat.

```bash
docker compose -f "docker-compose.yml" up -d --build
```

Pour finir, supprimez à la ligne 15 `-format` et relancez vos conteneurs

```bash
docker compose -f "docker-compose.yml" up -d --build
```
Vérifiez le bon fonctionnement du cluster sur votre navigateur en tapant l'ip de votre machine `http://<ip>:9870` ou votre localhost `http://127.0.0.1:9870` sur le port 9870.

