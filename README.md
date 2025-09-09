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
## 📂 1. Navigation dans le système de fichiers
### La commande **pwd** :
- Permet de déterminer dans quel dossier on se trouve actuellement
- Il donne le chemin complet du dossier actif
- Sa syntaxe est : 
```bash
pwd [Option (facultatif)]
```

#### Options :
- **-P** : Affiche le vrai chemin si celui-ci est un chemin symbolique.
<img width="547" height="98" alt="image" src="https://github.com/user-attachments/assets/8844906a-8ecf-482d-906a-6ad5fa7b778a" />

- **-P** : Affiche le chemin réel sur le disque en cas de chemin symbolique
<img width="935" height="95" alt="image" src="https://github.com/user-attachments/assets/35295a58-cdf0-4542-93a2-72f95377f4f4" />

### La commande **ls** :
- Permet d'afficher, lister les fichiers et dossier d'un répertoire
- Sa syntaxe est : 
```bash
ls [Option]... [fichier|dossier]...
```
#### Options :
- **-a** : Affiche tous les fichiers, même les fichiers cachés (qui commencent par .).
- **-l** : Affiche en liste détaillée (droits, propriétaire, taille, date).
- **-h** : Affiche les tailles en format lisible (Ko, Mo, Go). Souvent utilisé avec -l.
- **-d** : Affiche uniquement le nom du dossier (et pas son contenu).
- **-R** : Affiche le contenu des sous-dossiers récursivement.
- **-S** : Trie par taille (du plus gros au plus petit).
- **-t** : Trie par date de modification (les plus récents d’abord).
- **-r** : Inverse l’ordre du tri (utile avec -t ou -S).
- **-i** : Affiche l’inode de chaque fichier (identifiant interne Linux).
- **-F** : Ajoute un symbole après chaque nom : / pour dossier, * pour exécutable, etc.
- **--color=auto** : Colore automatiquement les résultats (dossiers en bleu, exécutables en vert, etc.).
<img width="939" height="934" alt="image" src="https://github.com/user-attachments/assets/287a8a67-1d90-4f11-aa9e-6d4ec8039f5e" />

### La commande **cd** :

---
## 📁 2. Gestion des fichiers et dossiers

---
## 📖 3. Lecture et affichage de fichiers

---
## 🔎 4. Recherche

---
## ⚙️ 5. Informations système

---
## 🔑 6. Gestion des droits

---
## 📦 7. Gestion des paquets (Debian, Ubuntu, Kali)
---
## 🌍 8. Réseau
---

## ✅ Conclusion  
Apprendre la ligne de commande sous Kali Linux est une étape incontournable pour progresser en cybersécurité.  
Avec de la pratique, tu pourras :  
- Gagner du temps dans la gestion de ton système.  
- Utiliser efficacement les outils Kali.  
- Automatiser des tâches de pentest.  
