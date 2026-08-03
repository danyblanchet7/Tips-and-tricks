#  Guide et Aide-Mémoire Bash (Linux / WSL)


> *"L'interface graphique permet de faire ce qui a été prévu. Le bash permet de faire tout le reste!"* 
>*"C'est comme utiliser Ocelet pour manipuler des fichiers SIG au lieu d'utiliser SAGA en clique-bouton"* 


---

  **Pourquoi utiliser la ligne de commande (Bash) ?**

1. La quasi-totalité des modèles d'IA, des bibliothèques de calcul (PyTorch, TensorFlow) et des serveurs de calcul (Cloud, GPU distants) tournent sous Linux.
2.  Une action qui prend 10 clics et 2 minutes à la souris (créer 50 dossiers, renommer des centaines de fichiers, filtrer des données) s'exécute en *une seule ligne de commande en quelques millisecondes*.
3. Il est difficile d'expliquer à un bro « sur quoi cliquer », par contre, lui partager un script ou une commande Bash garantit qu'il obtiendra exactement le même résultat.

---

##  Le meilleur des deux mondes = **Windows + WSL**

Il n'y a plus à choisir entre l'ergonomie de Windows et la puissance de Linux :
* **Windows** gère votre l'environnement graphique quotidien, les écrans et le matériel (notamment la carte graphique GPU).
* **Linux (WSL)** s'exécute en arrière-plan pour gérer les projets, les scripts Bash, les environnement de modélisation et les dépôts Git.

> **Ce guide a pour objectif** de rassembler les commandes, raccourcis et automatismes essentiels pour naviguer sereinement dans cet environnement hybride sans perdre de temps.

---

##  Navigation & Dossiers

- `pwd` : Affiche le dossier actuel.
- `ls` Liste le contenu du dossier
- `ls -la` : Affiche tous les fichiers (y compris les fichiers cachés) avec leurs détails.
- `cd <dossier>` : Se déplace dans un dossier - `cd ..` pour remonter d'un niveau.
- `cd ~` : Va dans ton home
- `cd -` : Retourne au dossier précédent

- `mkdir <nom>` : Crée un nouveau dossier.
- `rmdir <nom>` : Supprime un dossier vide.

---

## Fichiers & Édition

- `touch <fichier>` : Crée un fichier vide.
- `cp <source> <dest>` : Copie un fichier.
- `mv <source> <dest>` : Déplace ou renomme un fichier.
- `rm <fichier>` : Supprime un fichier.
- `rm -r <dossier>` : Supprime un dossier et tout son contenu.

- `head -n 10 fichier` Affiche les 10 premières lignes
- `tail -n 10 fichier` Affiche les 10 dernières lignes
- `nano fichier` Édite un fichier (simple)


---

##  Recherche 

- `clear` (ou `Ctrl+L`) : Nettoie la console.
- `find . -name "*.md"` : Cherche tous les fichiers Markdown à partir du dossier actuel.
- `grep "mot" fichier.txt` : Cherche un mot précis à l'intérieur d'un fichier.
- `cat <fichier>` : Affiche le contenu d'un fichier texte dans le terminal.

--

##  Exécution  


- `python3 script.py` Lance un script Python
-`bash script.sh ` Lance un script bash
-`chmod +x script.sh` Rend un script exécutable
- `./script.sh` Exécute un script local


## Variables et environnement
- `VAR="valeur"`    Définit une variable
-`echo $VAR`   Affiche la valeur d'une variable
- `export VAR="val"` : Rend la variable globale
- `echo 'export ...' >> ~/.bashrc` Rend permanent au démarrage
- `source ~/.bashrc` Recharge la config bash
-`which python3` Trouver où est installé un programme

## Installation de pakages
-`sudo apt install nom ` : Installe un paquet (Ubuntu)
- `sudo apt update`Met à jour la liste des paquets
- `pip install nom` : Installe un paquet Python

##  Utilitaires divers
-`df -h` : Espace disque disponible
du -sh dossier
Taille d'un dossier
- `tar xzvf fichier.tar.gz ` Décompresse une archive
- `tar czvf out.tar.gz dossier ` Compresse un dossier
history


## Raccourci clavier


### 1.  Déplacer le curseur (Navigation)

| Raccourci | Action |
| :--- | :--- |
| `Ctrl + A` | Déplace le curseur au **début** de la ligne. |
| `Ctrl + E` | Déplace le curseur à la **fin** de la ligne (*End*). |
| `Alt + F` | Avance le curseur d'un **mot** vers la droite (*Forward*). |
| `Alt + B` | Recule le curseur d'un **mot** vers la gauche (*Backward*). |

---

### 2.  Effacer et corriger du texte

| Raccourci | Action |
| :--- | :--- |
| `Ctrl + U` | Supprime tout du curseur jusqu'au **début** de la ligne. |
| `Ctrl + K` | Supprime tout du curseur jusqu'à la **fin** de la ligne (*Kill*). |
| `Ctrl + W` | Supprime le **mot juste avant** le curseur. |
| `Ctrl + Y` | Reposte / Colle le dernier texte effacé (*Yank*). |

---

### 3.  Retrouver l'historique des commandes

| Raccourci | Action |
| :--- | :--- |
| `Ctrl + R` | **Recherche interactive** dans l'historique (tape un mot-clé). |
| `Ctrl + G` | Quitte la recherche `Ctrl + R` sans exécuter de commande. |
| `Flèche Haut / Bas` | Fait défiler les commandes précédentes une par une. |

---

### 4.  Contrôle du terminal et des processus

| Raccourci | Action |
| :--- | :--- |
| `Tabulation` (`Tab`) | **Autocomplétion** automatique des chemins, dossiers et commandes. |
| `Ctrl + L` | Nettoie l'écran du terminal (équivalent de `clear`). |
| `Ctrl + C` | **Interrompt / Annule** la commande ou le script en cours. |
| `Ctrl + D` | Ferme la session Bash actuelle (équivalent de `exit`).



## Couleur des fichiers dans le bash 

| Couleur | Type de fichier | Explication |
| :--- | :--- | :--- |
| Blanc  | Fichier régulier | Un fichier texte, un document, une image, etc. (README.md, index.html). |
| Bleu | Répertoire (Dossier) | Un dossier qui contient d'autres fichiers ou sous-dossiers (/home, CLASSIC/). |
| Vert | Fichier exécutable | Un script ou un programme qui a les permissions d'exécution (script.sh, un binaire). | 