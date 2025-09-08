# 🖥️ Guide d’Introduction à la Ligne de Commande avec Kali Linux  

## 📌 Introduction  
La ligne de commande (aussi appelée **terminal** ou **shell**) est un outil puissant qui permet d’interagir directement avec le système d’exploitation.  
Sur **Kali Linux**, la ligne de commande est essentielle pour :  
- Naviguer dans les fichiers et gérer le système.  
- Lancer des programmes et des scripts de sécurité.  
- Installer et mettre à jour des outils de pentesting.  
- Automatiser des tâches d’administration et de cybersécurité.  

L’objectif de ce guide est de fournir une **introduction progressive** à l’utilisation de la ligne de commande sur Kali Linux, en commençant par les bases puis en abordant des commandes utiles en sécurité informatique.  

---

## 📚 Table des matières  

1. **Premiers pas avec le terminal**  
   - Ouvrir un terminal dans Kali  
   - Commandes de base : `whoami`, `pwd`, `clear`  

2. **Navigation dans le système de fichiers**  
   - Lister (`ls`)  
   - Se déplacer (`cd`)  
   - Chemins absolus et relatifs  

3. **Gestion des fichiers et répertoires**  
   - Créer (`touch`, `mkdir`)  
   - Supprimer (`rm`, `rmdir`)  
   - Copier/Déplacer (`cp`, `mv`)  

4. **Gestion des droits et utilisateurs**  
   - Vérifier les permissions (`ls -l`)  
   - Modifier les droits (`chmod`, `chown`)  
   - Utiliser `sudo`  

5. **Gestion des paquets dans Kali (APT)**  
   - Mettre à jour (`sudo apt update && sudo apt upgrade`)  
   - Installer un outil (`sudo apt install nmap`)  
   - Supprimer un outil (`sudo apt remove`)  

6. **Commandes réseau de base**  
   - Vérifier la connexion (`ping`, `curl`, `wget`)  
   - Trouver son IP (`ip a`, `ifconfig`)  
   - Scanner un réseau (`nmap`)  

7. **Gestion des processus et services**  
   - Voir les processus (`ps`, `top`, `htop`)  
   - Arrêter un processus (`kill`, `pkill`)  
   - Démarrer/Arrêter un service (`systemctl start/stop/restart`)  

8. **Compression et archives**  
   - Créer une archive (`tar`, `zip`)  
   - Extraire (`unzip`, `tar -xvf`)  

9. **Scripts Bash de base**  
   - Variables et echo  
   - Boucles et conditions  
   - Exemple : script pour automatiser une sauvegarde  

10. **Commandes utiles en cybersécurité (Kali)**  
   - `nmap` : scan de réseau  
   - `netcat` : communication réseau  
   - `hydra` : brute force de mots de passe  
   - `msfconsole` : Metasploit Framework  

---

## ✅ Conclusion  
Apprendre la ligne de commande sous Kali Linux est une étape incontournable pour progresser en cybersécurité.  
Avec de la pratique, tu pourras :  
- Gagner du temps dans la gestion de ton système.  
- Utiliser efficacement les outils Kali.  
- Automatiser des tâches de pentest.  
