

<p align="center">
  <img src="https://repository-images.githubusercontent.com/186841818/8aa95700-7730-11e9-84be-e80f28520325" width="100" alt="norsiide">
</p>
# Evobot

**Bot Music Discord — *ATTENTION : je ne suis pas le créateur du bot. Ce tutoriel explique uniquement comment j’ai réalisé mon installation.***
### Contact

* **Discord** : [Rejoins notre communauté](https://discord.gg/EV3fAhFZJT)
* **Website** : [Plus d'information](https://norsiide.be)
---

# 📑 Table des matières

* [Evobot](#evobot)
* [Table des matières](#-table-des-matières)
* [Configuration NGINX (vHost)](#configuration-nginx-vhost)

  * [Contact](#contact)
* [Installation du serveur](#installation-du-serveur)

  * [1. Mise à jour des paquets](#1-mise-à-jour-des-paquets)
  * [2. Installation de Node.js & npm](#2-installation-de-nodejs--npm)
* [Installation d’Evobot](#installation-devobot)

  * [1. Se placer dans le dossier](#1-se-placer-dans-le-dossier)
  * [2. Télécharger les fichiers](#2-télécharger-les-fichiers)
  * [3. Se déplacer dans le dossier du bot](#3-se-déplacer-dans-le-dossier-du-bot)
  * [4. Installer les dépendances](#4-installer-les-dépendances)
  * [5. Lancer le bot](#5-lancer-le-bot)
* [Service systemd](#service-systemd)

  * [Commandes systemd](#commandes-systemd)

---

## Tutoriel d'evobot


---

# Installation du serveur

### 1. Mise à jour des paquets

```bash
apt update && apt upgrade && apt install sudo curl
```

### 2. Installation de Node.js & npm

```bash
apt install nodejs npm
```

---

# Installation d’Evobot

### 1. Se placer dans le dossier

```bash
cd /mnt/
```

### 2. Télécharger les fichiers

```bash
git clone https://github.com/eritislami/evobot.git
```

### 3. Se déplacer dans le dossier du bot

```bash
cd /mnt/evobot
```

### 4. Installer les dépendances

```bash
npm install
```

### 5. Lancer le bot

```bash
npm run start
```

---

# Service systemd

Copiez le fichier `music.service` dans :

```
/etc/systemd/system/
```

---

## Commandes systemd

### Recharger systemctl

```bash
systemctl daemon-reload
```

### Activer au démarrage

```bash
systemctl enable music
```

### Gestion du service

```bash
systemctl start music
systemctl stop music
systemctl restart music
systemctl status music
```

ou :

```bash
service music start
service music stop
service music restart
service music status
```

---