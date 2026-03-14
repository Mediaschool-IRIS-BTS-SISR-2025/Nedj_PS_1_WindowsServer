# Automatisation du déploiement de services Windows Server 2022 via un menu PowerShell interactif

## 📋 Contexte

Dans le cadre d'un atelier BTS SIO option SISR, développement d'un outil d'automatisation permettant de déployer et configurer l'ensemble des services d'un Windows Server 2022 via un menu interactif en PowerShell. L'objectif était de réduire le temps de configuration manuelle tout en garantissant une installation reproductible et documentée.

---

## 🎯 Objectif

Concevoir et développer un menu PowerShell interactif permettant à un administrateur de déployer en quelques minutes l'ensemble des services d'un serveur Windows (AD DS, DNS, DHCP, OUs, groupes, utilisateurs) sans intervention graphique.

---

## 🛠️ Technologies utilisées

| Technologie | Rôle |
|---|---|
| PowerShell | Langage de script et moteur du menu interactif |
| Windows Server 2022 | Système cible du déploiement |
| Active Directory (AD DS) | Service déployé et configuré via les scripts |
| DNS & DHCP | Services réseau automatisés |
| Visual Studio Code | Environnement de développement |
| Oracle VirtualBox | Environnement de virtualisation et de test |

---

## ⚙️ Ce qui a été réalisé

### Structure du projet

```
Nedj_PS_1/
├── main.ps1              ← Menu principal interactif
├── 1-rename.ps1          ← Renommage du serveur
├── 2-ipconfig.ps1        ← Configuration IP statique
├── 3-install-roles.ps1   ← Installation des rôles AD, DNS, DHCP
├── 4-configure-adds.ps1  ← Configuration Active Directory
├── 5-configure-dns.ps1   ← Configuration DNS
├── 6-configure-dhcp.ps1  ← Configuration DHCP
├── 7-add-ou.ps1          ← Création des Unités Organisationnelles
├── 8-add-group.ps1       ← Création des groupes AD
├── 9-add-user.ps1        ← Création des utilisateurs
├── 10-import-csv.ps1     ← Import en masse depuis fichier CSV
└── 11-exit.ps1           ← Quitter le menu
```

### Fonctionnalités du menu interactif

| Option | Action |
|---|---|
| [1] | Renommer le serveur |
| [2] | Configurer l'adresse IP statique |
| [3] | Installer les rôles AD DS, DNS, DHCP |
| [4] | Configurer Active Directory et promouvoir le DC |
| [5] | Configurer le service DNS |
| [6] | Configurer le service DHCP |
| [7] | Créer les Unités Organisationnelles |
| [8] | Créer les groupes dans l'AD |
| [9] | Créer les utilisateurs manuellement |
| [10] | Importer des utilisateurs depuis un fichier CSV |
| [11] | Quitter |

### Points techniques clés
- Vérification des droits administrateur au lancement
- Gestion des erreurs avec messages explicites à chaque étape
- Import CSV permettant la création en masse de comptes utilisateurs
- Chaque script est indépendant et peut être exécuté séparément

---

## ✅ Résultats obtenus

- Menu opérationnel permettant de déployer un serveur complet en moins de 30 minutes
- Déploiement testé et validé sur VM Windows Server 2022 sous VirtualBox
- Code versionné et disponible sur GitHub

---

## 🔗 Compétences BTS SIO mobilisées

| Compétence | Description |
|---|---|
| **B1.1** | Gérer le patrimoine informatique (automatisation de la configuration) |
| **B1.5** | Mettre à disposition des utilisateurs un service informatique |

---

## 👤 Auteur

**Nedjmeddine Belloum** — BTS SIO option SISR  
Centre de formation : Mediaschool Nice — IRIS  
Période : 14/05/2025 au 25/05/2025  
