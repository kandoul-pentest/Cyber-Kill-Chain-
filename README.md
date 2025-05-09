# Cyber-Kill-Chain soc level 1 
The Cyber Kill Chain framework is designed for identification and prevention of the network intrusions. You will learn what the adversaries need to do in order to achieve their goals.
<!-- SCREENSHOT 1 - HEADER -->
![Schéma de la Cyber Kill Chain](soc1path.jpeg)  
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

## 3. Delivery (Livraison)
**Définition** :  
Transmission du payload malveillant à la cible.


### 4. exploitation
Phase where the attacker activates their malicious code after infiltrating the system.

### 🔧 Common Techniques  
1. **Software vulnerability exploitation**  
   Example: `CVE-2023-1234` (buffer overflow)

2. **Malicious documents**  
   ```vba
   ' Simplified malicious Word macro
   Sub AutoOpen()
       Shell "cmd /c powershell -nop -w hidden -e JABzAD0A..."
   End Sub

   
 ## 5. Installation (Persistance)

### 🎯 Définition
Phase où l'attaquant s'installe durablement dans le système.

## 🕹6. Command & Control (C2)

### 🔌 Définition
Mécanisme permettant aux attaquants de **contrôler à distance** les machines compromises.

## 7. Actions on Objectives (Exfiltration)

### 🎯 Définition
Phase finale où l'attaquant **réalise son objectif** (vol de données, sabotage, etc.).
## 🔍 Practice Analysis - Target Breach 2013

### 📸 Attack Flow Visualization
![Target Breach Kill Chain](task.jpeg)  
*Visual breakdown of the Target Corporation cyberattack*

### 🔗 Kill Chain Mapping
```mermaid
graph TD
    A[Recon: HVAC Vendor] --> B[Weapon: Malware]
    B --> C[Delivery: Vendor Portal]
    C --> D[Exploit: Credential Theft]
    D --> E[Lateral Movement]
    E --> F[POS Data Exfiltration]
