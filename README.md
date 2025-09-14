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
- Syntaxe :
```bash
rmdir [OPTIONS] DOSSIER...
```
##### Options :
- **-p** : Supprime aussi les parents vides
- **-v** : Affiche un message pour chaque suppression
---
## 📖 3. Lecture et affichage de fichiers
### La commande cat :
- Permet d'afficher les contenus d'un fichier dans le terminal
- Permet de créer un fichier avec **>**
- Permet de concaténer (coller) plusieurs fichiers en un seul
- Rediriger du texte ou un contenu dans un autre fichier.
- Syntaxe :
```bash
cat [OPTION]... [FICHIER]...
```
#### Options :
- **-n** : Numérote toutes les lignes
- **-b**  : Numérote seulement les lignes non vides
- **-s** : Supprime les lignes vides répétées (n’en garde qu’une seule)
- **-E** : Montre un $ à la fin de chaque ligne (pour voir les retours à la ligne)
- **-T** : Affiche les tabulations comme ^I
- **-A** : Affiche tout (équivaut à -vET, pratique pour déboguer
- **-v** : Affiche les caractères non imprimables (mais pas \n et \t)

<img width="951" height="108" alt="image" src="https://github.com/user-attachments/assets/f9f2553a-d53b-4782-ab2d-cc84b9b72bee" />

### La commande less:
- Permet de lire un fichier page par page (sans tout afficher d’un coup).
C’est très utile pour parcourir de gros fichiers de logs (ex : /var/log/auth.log).
- Pour sortir de la lecture, on clique sur la touche **Q/q**
- Pour chercher un mot, on utilise **/mot à chercher**
- Syntaxe :
```bash
less [options] fichier
```
#### Options :
- **-N** : Affuche les numéro de ligne
-**+F** : suivre en temps réel les nouvelles lignes

### La commande head:
- Permet d'afficher la premier ligne d'un fichier (par défaut)
- Syntaxe :
```bash
head [options] fichier
```
#### Options :
- **-n x** :  Affiche les X premières lignes
- **-c X** : Affiche les X premiers caractères (ou octets)
<img width="957" height="581" alt="image" src="https://github.com/user-attachments/assets/7078b8e8-55be-4289-b9d1-5d7a916789d0" />
 
### La commande tail:
- Permet d'afficher les dernières lignes d'un fichier
- On peut surveiller un fichier en temps réels (comme de log)
- Syntaxe :
```bash
tail [options] fichier
```
#### Options :
- **-n x**: afficher les X dernières lignes
- **-f** : suivre en temps réel les nouvelles lignes (ex: quand un fichier log s’actualise)
- **-c x** : afficher les X derniers caractères
<img width="941" height="939" alt="image" src="https://github.com/user-attachments/assets/77d8ad74-375c-4c43-864c-8849917127f1" />

### La commande nl:
- Affiche le contenu d’un fichier avec numéros de ligne (similaire à cat -n mais plus flexible).
- Syntaxe :
```bash
nl [options] fichier
```

#### Options : 
- **-b a** : numéroter toutes les lignes
- **-b t** : numéroter uniquement les lignes non vides (par défaut)

<img width="938" height="701" alt="image" src="https://github.com/user-attachments/assets/19886297-db1f-4469-a4d8-63d085b9cebc" />

### La commande more:
- Comme less 
---
## 🔎 4. Recherche
### La commande find:
- Permet de rechercher des fichiers/dossiers selon leur nom, type, taille, date, permissions, etc.
- Syntaxe :
```bash
find chemin [options] [expression]
```

#### Options :
- **-name "fichier"** : chercher par nom
- **-iname** : chercher par nom, sans tenir compte des maj/min
- **-type f** : recherche par fichier uniquement
- **-type d** : Recherche par dossier uniquement
- **-size +10M** : fichiers de plus de 10 Mo
- **-perm 644** : fichiers avec permission exacte 644
- **-user utilisateur** : fichiers appartenant à un utilisateur
- **-exec commande {} \;** : exécuter une commande sur chaque résultat
<img width="938" height="356" alt="image" src="https://github.com/user-attachments/assets/0cda9c80-11d3-4077-905e-574864df20da" />

### La commande grep:
- Cherche un mot ou motif (pattern) dans un fichier ou un flux.
- syntaxe
```bash
grep [options] "mot" fichier
```
#### Options : 
- **-i**: ignore la casse (maj/min)
- **-n**: affiche le numéro de ligne
- **-r**: recherche récursive dans un dossier
- **-v**: inverse : affiche les lignes qui ne contiennent pas le mot
- **-E**: active les expressions régulières avancées (regex)
- **-color=auto**: surligner les correspondances
<img width="958" height="154" alt="image" src="https://github.com/user-attachments/assets/204d44ce-941f-4520-a299-0439251dc072" />

### La commande egrep:
- Comme grep, mais pour utiliser plus facilement les regex avancées.
- équivalent de grep -E
- Exemple
<img width="961" height="154" alt="image" src="https://github.com/user-attachments/assets/051a815d-adf7-4f92-8a84-b2d30c030e93" />
**Cherche root ou admin.**
  
### La commande locate:
- Utilise une base de données indexée → beaucoup plus rapide que find.
- Nécessite de mettre à jour la base avec **updatedb**.
- syntaxe
```bash
locate mot
```

### La commande which / whereis/ type:
- Utiles pour savoir où est installé un programme
- **which**: donne le chemin d’un binaire dans $PATH
- **whereis**: donne le chemin + doc man + source (si dispo)
- **type**: indique si une commande est un binaire, un alias, une fonction…

---
## ⚙️ 5. Informations système

- **uname -a** : Donne toutes les infos du noyau (version Linux, architecture, etc.).
![Uploading image.png…]()

- **lsb_release -a** : Donne la version de la distribution (ex: Debian 12, Ubuntu 22.04, Kali).
- **cat /etc/os-release** : Affiche les infos système
- **lscpu** : Donne les infos du processeur.
- **free -h** : Affiche la mémoire RAM dispo/occupée.
- **top/htop** : Surveille en temps réel l’utilisation CPU/mémoire/processus.
- **df -h** : Utilisation des disques (taille, espace libre).
- **du -sh /var/log** : Taille totale d’un dossier.
- **lsblk** : Liste les disques et partitions.
---
## 🔑 6. Gestion des droits
- **chmod permisions fichier** : Change les permissions
- **chown utilisateur:group fichier** : Change l’utilisateur et groupe propriétaire.

----
## 🌍 7. Réseau
---
- **ping** : Teste la connexion internet
- **ip a** : Affiche ous les adresses IP
- **hostname -I** : Affiche uniquement l’adresse IP locale.
- **ip route** : Affiche la route réseau (passerelle, etc.).
- **ss -tulnp** : Liste les ports ouverts et les processus associés.
- **nslookup/dig** : Résout le nom de domaine vers une IP.
- **tcpdump -i eth0** : Capture le trafic réseau sur l’interface eth0
- **iftop** : Surveille la bande passante en temps réel (si installé).

## 8. Autres
- **strings fichier** : extrait le texte lisible d’un binaire
- **uptime**` : depuis combien de temps tourne la machine
## ✅ Conclusion  
Apprendre la ligne de commande sous Kali Linux est une étape incontournable pour progresser en cybersécurité.  
Avec de la pratique, tu pourras :  
- Gagner du temps dans la gestion de ton système.  
- Utiliser efficacement les outils Kali.  
- Automatiser des tâches de pentest.  
