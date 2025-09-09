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
-  La commande cd (change directory) permet de changer de dossier courant dans le terminal.
-  C’est comme “naviguer” dans les dossiers de ton ordinateur.
-  Syntaxe
```bash
cd [Chemins | raccourcis]
```
#### Raccourcis
- **cd Dossier** : Entrer dans un dossier du répertoire courant.
- **cd** : Aller dans ton dossier personnel (home).
- **cd ..** : Remonter d’un niveau (dossier parent).
- **cd /** : Aller à la racine du système.
- **cd -** : Revenir au dossier précédent.
- **cd ~/Documents** : Aller dans le dossier Documents de ton home.
- **cd /chemin/absolu** : Aller dans un dossier en utilisant son chemin complet.

<img width="933" height="378" alt="image" src="https://github.com/user-attachments/assets/5bccd164-3263-4e84-8a5f-b8f717613231" />

---
## 📁 2. Gestion des fichiers et dossiers
### La commande touch :
- Permet de créer un fichier vide s'il n'existe pas
- Mettre à jour la date et l’heure d’accès/modification d’un fichier existant.
- Syntaxe :
```bash
touch [OPTION]... FICHIER...
```
##### Options : 
- **-a** : Change uniquement la date d’accès (last access time).
- **-m** : Change uniquement la date de modification (last modification time).
- **-c** : Ne crée pas de fichier s’il n’existe pas.
- **-d** : Fixe une date spécifique en lisant une chaîne (format libre, style “2025-09-09 12:00”).

<img width="945" height="414" alt="image" src="https://github.com/user-attachments/assets/528da9ed-2206-4f21-8dbb-61cf135cc781" />

### La commande mkdir :
- Permet de créer un ou plusieurs dossiers (répertoires)
- Syntaxe :
```bash
mkdir [OPTION]... DOSSIER...
```
##### Options :
- **-p** : Crée aussi les dossiers parents manquants (sinon mkdir échoue).
- **-m** : Définit les permissions du dossier à la création (comme chmod).
- **-v** :  Affiche les messages lors de la création d'un dossier
<img width="947" height="849" alt="image" src="https://github.com/user-attachments/assets/f3ccac26-18a9-42db-b45b-fc5db07ed465" />

### La commande cp :
- Permet de copier un fichier ou dossier
- Il ecrasse les contenues
- Syntaxe :
```bash
cp [OPTIONS] SOURCE... DESTINATION
```
##### Options :
- **-i** : Demande confirmation avant d’écraser
- **-f** : Force la copie (écrase sans demander)
- **-n** : N’écrase jamais les fichiers existants
- **-v** : Mode bavard (affiche les actions)
- **-u** : Copie seulement si le fichier source est plus récent
- **-r ou -R** : Copie récursive (dossiers et sous-dossiers)
- **-a** : Archive : garde permissions, liens, timestamps
- **p** : Préserve permissions/dates du fichier
### La commande mv : 
- Permet de deplacer un fichier ou un dossier
- Permet de renommer un fichier ou un dossier
- Syntaxe :
```bash
mv [OPTIONS] SOURCE... DESTINATION
```
##### Options :
- **-i** : Demande confirmation avant d’écraser
- **-f** : Force la copie (écrase sans demander)
- **-n** : N’écrase jamais les fichiers existants
- **-v** : Mode bavard (affiche les actions)
  
### La commande rm : 
- Permet de supprimer un fichier ou un dossier
- Syntaxe :
```bash
rm [OPTIONS] DOSSIER...
```
##### Options :
- **-i** : Demande confirmation avant d’écraser
- **-f** : Force la suppression (écrase sans demander)
- **-v** : Mode bavard (affiche les actions)
- **-r ou -R** : Suppression récursive (dossiers + contenu)
- **-d** : Supprime des dossiers vides (comme rmdir)
### La commande rmdir : 
- Permet de supprimer un dossier vides
- - Syntaxe :
```bash
rmdir [OPTIONS] DOSSIER...
```
##### Options :
- **-p** : Supprime aussi les parents vides
- **-v** : Affiche un message pour chaque suppression
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
