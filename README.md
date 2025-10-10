# 🖥️ SN2 - Installation et configuration d'un firewall
## 🛠️ Étapes de l’atelier

---
## 📌 Pré-requis
❗ Toutes les machines virtuelles ne sont pas à allumer en même temps ❗
- Une machine virtuelle **Ubuntu** (ou dérivé: Debian, Linux Mint... )
- Une machine virtuelle **RockyLinux** (ou dérivé: AlmaLinux, CentOS... )
- Une machine virtuelle **Windows Server**
- Connexion réseau entre serveur et client.
- Doit être persistent ( Résiste au redémarrage )
---

### 1️⃣ Installation et configuration d'UFW
- Installer un service WEB
- Installer le service du firewall UFW
- Essayer de joindre le service HTTP
- Configurer UFW pour laisser passer le traffic entrant HTTP
---

### 2️⃣ Installation et configuration de Firewalld
- Installer un service WEB
- Installer le service du firewall Firewalld
- Essayer de joindre le service HTTP
- Configurer firewalld pour laisser passer le traffic entrant HTTP
---

### 3️⃣ Installation et configuration du pare-feu Windows Defender
- Installer IIS
- Désactivation de la règle par default dans trafic entrant (La page IIS ne doit plus être accessible) 
- Création d'une nouvelle règle entrante personnalisé
---


iptables

# Pare-feu réseau

## 🛠️ Étapes de l’atelier

---
## 📌 Pré-requis
- Une machine virtuelle **PFSense** avec 3 cartes réseaux ( 1 NAT et 2 LAN Segments)  
⚠️ Le bridge peut poser des soucis de niveau 2 avec la table ARP ⚠️
--- 

### 4️⃣ Installation et configuration d'un Firewall réseau avec PFSense (Réalisation possible avec OPNSense, IPFire, PaloAlto, Stormshield ...)
- Installer le PFSense et configurer les cartes de sorte que le WAN soit mis sur la carte réseau du NAT. Le LAN soit mis sur une carte réseau LAN Segment et la DMZ sur l'autre LAN Segment.
- Votre machine machine virtuelle qui se trouve dans le réseau Lan possède bien internet. Par default, PFSense créé une règle qui redirige tout le trafic LAN vers internet.
- Créer une redirection de port NAT pour permettre l'accès à votre serveur WEB depuis le WAN en 8080