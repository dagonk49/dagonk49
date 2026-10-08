<div align="center">

# Evann Bougoula · `dagonk49`

### Je pilote des projets informatiques avec l'IA.<br/>Elle code. Moi, je cadre, je relis, je corrige et je traque les failles.

Alternant technicien informatique à la **DSI régionale de l'Établissement Français du Sang** · **BTS SIO SISR** · Angers

[![Portfolio](https://img.shields.io/badge/Portfolio-evann--bougoula.dagz.fr-0a0a0c?style=for-the-badge&logo=googlechrome&logoColor=white)](https://evann-bougoula.dagz.fr)
[![NetForge](https://img.shields.io/badge/NetForge-netforge.dagz.fr-1f6feb?style=for-the-badge&logo=cisco&logoColor=white)](https://netforge.dagz.fr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-evann--bougoula-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/evann-bougoula)
[![CV](https://img.shields.io/badge/CV-PDF-444?style=for-the-badge&logo=readdotcv&logoColor=white)](https://evann-bougoula.dagz.fr/CV_Evann_Bougoula.pdf)

</div>

---

## 🧭 Mon approche

Je ne me présente pas comme développeur. Sur mes projets, **c'est l'IA qui écrit le code**. Mon travail, c'est tout le reste :

- **Cadrer** : partir d'un besoin réel, écrire le cahier des charges, découper le travail en missions claires avec des règles strictes.
- **Faire produire** : piloter des assistants de code IA (agents configurés avec instructions, mémoire et skills dédiés).
- **Relire et corriger** : vérifier ce qui sort, tester, lire les logs, renvoyer en correction quand ça ne tient pas.
- **Chercher les failles** : auditer la sécurité (entrées utilisateur, CORS, droits admin, secrets, fuites mémoire…).
- **Déployer et exploiter** : conteneuriser et faire tourner le tout sur mon propre HomeLab.

```mermaid
flowchart LR
    A[Besoin concret] --> B[Cahier des charges<br/>missions et règles]
    B --> C[L'IA code]
    C --> D[Je relis, je teste<br/>et je corrige]
    D --> E[Audit sécurité]
    E -->|bug ou faille| C
    E --> F[Déploiement<br/>Docker · HomeLab]
```

---

## 🚀 Projets concrets

### 🛰️ NetForge — du plan d'adressage à la console Cisco

> Outil web gratuit pour concevoir un réseau de A à Z, né d'un besoin rencontré en cours et en TP : découper les plages, suivre les attributions, écrire les configs… à la main, c'est long et source d'erreurs.

- Calcul **VLSM / FLSM** sur plusieurs réseaux parents, liens /31 et hôtes /32
- **VLAN, DHCP** et carte visuelle de l'espace d'adressage
- **Topologie en glisser-déposer** avec détection des boucles, des doublons d'IP et des liaisons de transit /30
- **Génération de configurations** pour 17 plateformes de 13 constructeurs (Cisco, Juniper, Aruba, Huawei, MikroTik, Fortinet, Palo Alto…) + scripts Windows, Linux et macOS
- Exports **PDF, PNG, TXT**
- **100 % local** : calculs dans le navigateur, projets en IndexedDB, sans compte ni traceur

**Mon rôle :** définir le besoin et le cahier de recette (cas VLSM, détection de chevauchement, trunks 802.1Q générés), valider les calculs d'adressage et les configs produites, imposer une conception sans collecte de données, conteneuriser et publier l'outil.

[![Ouvrir NetForge](https://img.shields.io/badge/▶_Ouvrir-NetForge-1f6feb?style=flat-square)](https://netforge.dagz.fr/app)
[![Docker Hub](https://img.shields.io/badge/Docker_Hub-dagonk%2Fnetforge--engine-2496ED?style=flat-square&logo=docker&logoColor=white)](https://hub.docker.com/r/dagonk/netforge-engine)
[![V4](https://img.shields.io/badge/Dépôt-NETFORGE--V4_(en_préparation)-555?style=flat-square&logo=github)](https://github.com/dagonk49/NETFORGE-V4)

---

### 🎬 DagzFlix — mon hub de streaming façon Netflix

> Interface de streaming et de découverte branchée sur mon serveur **Jellyfin** et sur **Jellyseerr / TMDB**. Quatre itérations publiques, de la V0 à la V4.

- Algorithme de recommandation maison **DagzRank** (score sur 7 couches : genres favoris, historique, notes, fraîcheur, télémétrie…)
- **Contrôle parental** par rôles (admin / adulte / enfant) et **panneau d'administration**
- Lecteur **HLS** multi-pistes audio et sous-titres, reprise intelligente des séries, favoris, notes
- Stack : Next.js 14 avec BFF + MongoDB (v3) · React + FastAPI (V4)

**Ce que montre ce projet côté pilotage :**

| | |
|---|---|
| 📋 **Versioning imposé à l'IA** | 19 versions documentées en 8 jours (V0,001 → V0,011) : chaque demande = date, objectif, fichiers touchés, validation |
| 🐛 **Débogage sur logs réels** | 3 rounds d'analyse après une régression, jusqu'à **0 erreur 500** sur la session de monitoring |
| 🛡️ **Audit sécurité (V0,009)** | Validation des entrées avec Zod, assainissement des identifiants, contrôle d'origine CORS, contrôle admin centralisé, proxy d'images en streaming contre les fuites mémoire |
| 🏗️ **Refactoring** | Un fichier de **3 275 lignes** découpé en **11 modules**, contrat d'API strictement identique (25 GET + 13 POST) |
| 🔐 **Sécurité dès la conception (V4)** | Hachage Argon2id, chiffrement AES-256-GCM des clés API, cookies HttpOnly / SameSite Strict, rate limiting, en-têtes de sécurité |

[![v3](https://img.shields.io/badge/Dépôt-DagzFlix_v3-555?style=flat-square&logo=github)](https://github.com/dagonk49/v3)
[![V4](https://img.shields.io/badge/Dépôt-DagzFlix_V4-555?style=flat-square&logo=github)](https://github.com/dagonk49/dagzflixV4)

---

### 🧪 EVANN // ROOT ACCESS — un portfolio qui se joue

> [evann-bougoula.dagz.fr](https://evann-bougoula.dagz.fr) : une lecture sobre et accessible pour aller à l'essentiel, ou un **lab 3D** où l'on remet une petite infrastructure en ligne.

- **Mission réseau simulée** : brassage, VLAN d'accès, adressage IPv4, diagnostic `ipconfig` / `ping` calculé à partir de l'état du lab
- **Terminal CLI** intégré et circuit 3D extérieur avec physique de véhicule
- Une seule source de données pour le mode sobre, le mode 3D et le terminal
- Aucun cookie publicitaire, aucune mesure d'audience, référencement travaillé
- Stack : Next.js, React, TypeScript, Three.js, Rapier

[![Portfolio](https://img.shields.io/badge/Dépôt-portefolio--Evann--BOUGOULA-555?style=flat-square&logo=github)](https://github.com/dagonk49/portefolio-Evann-BOUGOULA)

---

### 🏠 HomeLab — l'infra qui fait tourner tout ça

> L'IA écrit le code. L'hébergement, le réseau et la sécurité de l'infrastructure, c'est mon terrain.

- **Proxmox VE** : une VM Docker principale (plus de la moitié des ressources) qui héberge NetForge, ce portfolio, Jellyfin, un staging privé et des automatisations
- **VM de test** : Windows Server 2022 et 2025, Debian, Windows 11
- **Sécurisation** : segmentation VLAN, accès distant par **WireGuard**, publication des services derrière **Nginx Proxy Manager**

---

## 🛠️ En entreprise

| Où | Ce que j'y fais / fait |
|---|---|
| **EFS** · DSI régionale (alternance, depuis 2026) | Support N1, gestion des comptes et accès Active Directory, masterisation et déploiement du parc, programme national AMI |
| **NET4BUSINESS** (stage 2026) | Support d'installation Windows automatisé et personnalisé avec **Ventoy** |
| **NET4BUSINESS** (stage 2025) | Hyperviseur **Proxmox VE sous Debian** + script de nettoyage des applications Windows |
| **NET4BUSINESS** (stage 2024) | Wi-Fi **Ubiquiti UniFi** avec réseaux invités et privé isolés par VLAN |

🎓 **BTS SIO SISR** (MyDigitalSchool Angers, 2026-2028) · **Bac Pro CIEL** mention très bien
📜 Cisco Networking Academy (introduction à la cybersécurité) · Pix · SST · Habilitation électrique B1V

---

## 🧰 Outils

**Infra & réseau**

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=flat-square&logo=proxmox&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=flat-square&logo=debian&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D4?style=flat-square&logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active_Directory-003366?style=flat-square)
![Cisco IOS](https://img.shields.io/badge/Cisco_IOS-1BA0D7?style=flat-square&logo=cisco&logoColor=white)
![Ubiquiti](https://img.shields.io/badge/UniFi-0559C9?style=flat-square&logo=ubiquiti&logoColor=white)
![WireGuard](https://img.shields.io/badge/WireGuard-88171A?style=flat-square&logo=wireguard&logoColor=white)
![Nginx Proxy Manager](https://img.shields.io/badge/Nginx_Proxy_Manager-F15833?style=flat-square&logo=nginxproxymanager&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Jellyfin](https://img.shields.io/badge/Jellyfin-00A4DC?style=flat-square&logo=jellyfin&logoColor=white)

**Technologies des projets que je pilote**

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**IA**

![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=claude&logoColor=white)
![Agents IA](https://img.shields.io/badge/Agents_de_code_IA-6E40C9?style=flat-square)

---

<div align="center">

**L'IA va vite. Mon job, c'est qu'elle aille dans la bonne direction, sans laisser de porte ouverte.**

📍 Angers · Nantes · Ancenis · Candé — présentiel ou télétravail

</div>
