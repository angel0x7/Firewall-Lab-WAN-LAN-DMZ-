## Lab Virtuel WAN / LAN / DMZ avec pfSense

Ce dépôt contient la configuration et la documentation de mon laboratoire virtuel **pfSense** structuré en trois zones réseau : WAN (Internet simulé), LAN (réseau interne) et DMZ (zone exposée pour le serveur web).

### 📂 Contenu du dépôt

- `Rapport_Lab_WAN_LAN_DMZ.pdf` : Rapport détaillé (PDF) présentant toutes les étapes de mise en place, avec captures d’écran et schémas visuels.
- **VM Configurations** : Scripts et instructions utilisés pour :
  - Installation et configuration de la VM **pfSense** (interfaces WAN, LAN, DMZ)
  - Mise en place des règles de firewall (LAN → DMZ, DMZ → Internet)
  - Règle NAT (Port Forward) pour exposer le serveur web depuis le WAN
- **Server Setup** : Guide d’installation du rôle **IIS** sur **Windows Server 2022** en DMZ.
- **Schémas et Captures** : Topologie réseau, paramètres VirtualBox, captures d’interface pfSense, configuration IIS.

### 🚀 Aperçu des fonctionnalités

1. **Segmentation réseau** :
   - Isolation stricte entre LAN et DMZ
   - DMZ limitée à DNS, HTTP, HTTPS sortant
2. **Pare-feu pfSense** :
   - Règles explicites pour chaque interface
   - Anti-Lockout pour l’administration
3. **Port Forwarding** :
   - Redirection du port 80 du WAN vers le serveur web en DMZ
4. **Serveur Web** :
   - Installation IIS sur Windows Server 2022
   - Page par défaut accessible depuis LAN et Internet

### 📖 Rapport détaillé

Vous trouverez dans le PDF toutes les explications détaillées, commandes, captures d’écran et schémas :

[Consulter le rapport complet (PDF)](Rapport_Lab_WAN_LAN_DMZ.pdf)

### 🔧 Installation & Exécution

1. Clonez ce dépôt :
   ```bash
   git clone https://github.com/AngelVelasco/Lab-pfSense-WAN-LAN-DMZ.git
   cd Lab-pfSense-WAN-LAN-DMZ
   ```
2. Ouvrez le **Rapport_Lab_WAN_LAN_DMZ.pdf** pour suivre les étapes.
3. Déployez vos VMs dans VirtualBox / VMware selon les instructions du rapport.

### 🎯 Perspectives d’évolution

- Publication via **HAProxy** (reverse proxy) & certificats **Let’s Encrypt**
- Ajout d’un **IDS/IPS** (Snort/Suricata)
- Déploiement de **VPN** (OpenVPN, IPsec)
- Supervision avancée (NetFlow, ELK Stack)

---

**Auteur** : Angel Velasco – Étudiant en cybersécurité (ECE Paris)
