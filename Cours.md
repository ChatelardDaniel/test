## <span style="color: blue">Git et GitHub</span>

### <span style="color: blue">1. Ligne de commande.</span>

<span style="color: lightgreen">a) Principe et fonctionnement de l'interface en ligne de commande</span>

<span style="color: yellow">ls</span> affiche la liste de tous les fichiers et dossiers.

<span style="color: yellow">ls -a</span> avec l'option (a), qui signifie (all),il affichera tous les fichiers du dossier courant, mêmes ceux qui sont cachés,
<span style="color: yellow">*dir /a*</span> sur windows.

<span style="color: yellow">ls -a Studi</span> affichera tous les fichiers, mêmes ceux cachés du dossier Studi.
<span style="color: yellow">dir /a Studi</span> sur windows.

<span style="color: yellow">(.)</span> point c'est le dossier courant, dans celui où nous sommes.

<span style="color: yellow">(..)</span> point point c'est le dossier parent.

<span style="color: yellow">nom de commande(ls) option (-a) paramètre un ou plusieurs (Studi).</span> séparés par des espaces, permettent de manipuler nos ordinateurs.

<span style="color: yellow">CLI</span> Command Line Interpreter, interpréteur de lignes de commande.

<span style="color: yellow">à retenir</span>
Les interfaces en ligne de commande sont disponibles sous tous les systèmes d'exploitation. Elles permettent de gérer toutes les tâches d'administration d'un système, de la simple manipulation de fichiers à la configuration des logiciels.

Même si son utilisation a l'air plus complexe à aborder, la ligne de commande est plus simple que de parcourir de nombreux menus de configuration, et permet l'automatisation des tâches d'administration.

Il existe plusieurs interpréteurs de lignes de commande selon les systèmes d'exploitation : chacun permet une syntaxe et des fonctionnalités différentes.



<span style="color: lightgreen">b) Ouvrir une invite de commande</span>

Pour de nombreuses commandes sur Linux, vous aurez besoin des privilèges Administrateur. Il faudra écrire votre commande en commençant par <span style="color: yellow">sudo</span> pour avoir une élévation de privilège. Votre mot de passe vous sera demandé la première fois.

Exemple : <span style="color: yellow">sudo apt-get update</span> pour mettre à jour le gestionnaire de paquets APT.

<span style="color: lightgreen">Ouvrir une interface de commande sur Windows</span>

<span style="color: lightgreen">Via un raccourci clavier :</span>

Le raccourci clavier peut être utilisé quelle que soit la version de Windows. Ouvrez la fenêtre Exécuter en appuyant simultanément sur les touches <span style="color: yellow">Windows+R</span>. La fenêtre Exécuter s'affiche. Dans la zone Ouvrir, tapez <span style="color: yellow">cmd</span>, puis cliquez sur OK.

<span style="color: lightgreen">Via le menu démarrer Windows 10 :</span>

Ouvrez le Menu Démarrer, puis tapez <span style="color: yellow">cmd</span> ou <span style="color: yellow">Invite de commandes</span> au clavier. Cliquez sur Invite de commandes (clic droit si vous voulez l'ouvrir en tant qu'administrateur).

Il existe des interfaces en ligne de commande, telles que GitBash, qui permettent de simuler des commandes Linux sur un environnement Windows. Il faut donc savoir, qu'avec ces lignes de commandes, nous n'avons pas forcément besoin de maîtriser toutes les commandes Windows.

<span style="color: lightgreen">c) Manipuler des dossiers et des fichiers</span>

<span style="color: yellow">cd</span> change directory, changer de répertoire sous Windows, Linux et macOS..
````markdown
cd / # permet de se déplacer à la racine du disque sous Linux
cd users # permet de se déplacer dans le dossier users du dossier courant, s'il existe
cd .. # permet de se déplacer dans le répertoire parent
cd /users/admin/desktop # permet d'accéder à un répertoire en utilisant son chemin absolu
````
<span style="color: yellow">cd ..</span> pour aller dans le dossier parent, remonte un cran en arrière. Idem pour windows.

<span style="color: yellow">cd /c:/Users/AC2A/Documents/Studi</span> avec un chemin absolu.

<span style="color: yellow">ls .</span> pour lister le dossier courant, <span style="color: yellow">dir .</span> pour windows. Le point est la valeur par défaut de ls
````markdown
ls # permet de lister le contenu du répertoire courant sur Linux et macOS
dir # permet de lister le contenu du répertoire courant sur Windows
ls /home/admin/ # permet de lister le contenu du répertoire admin depuis n'importe quel répertoire
````
<span style="color: yellow">le chemin relatif</span> est le chemin depuis notre répertoire actuel (courant) exemple: <span style="color: yellow">ls Studi</span>, affichera tout les fichiers de mon dossier studi. Le chemin relatif est aussi symboliser par le point <span style="color: yellow">(.)</span>



<span style="color: yellow">le chemin absolu</span> est le chemin depuis la racine de l'ordinateur, exemple: <span style="color: yellow">ls /c:/Users/AC2A/Documents/Studi</span>.
````markdown
/Users/admin/desktop/dossier1/ -> indique le chemin absolu vers le répertoire dossier1
````




<span style="color: yellow">mkdir</span>, permet de créer un répertoire aussi bien sous Windows que sous Linux et macOS.
````markdown
mkdir dossier1 # crée le dossier1 dans le dossier courant
mkdir C:\users\admin\desktop\dossier1 # créé le dossier1 en utilisant son chemin absolu sous Windows
mkdir /home/admin/desktop/dossier1 # créé le dossier1 en utilisant son chemin absolu sous Linux et macOS
````
<span style="color: yellow">touch</span>, création de fichier, <span style="color: yellow">echo</span> sous windows.
````markdown
echo "" > texte.txt # permet de créer le fichier nommé "texte.txt" sous Windows
touch texte.txt # permet de créer le fichier nommé "texte.txt" sous Linux et macOS
touch /home/admin/desktop/dossier1/texte.txt # crée le fichier "texte.txt" dans le dossier1 pour Linux
````
<span style="color: yellow">cp / mv</span>, <span style="color: yellow">copy / move</span>, permet de copier, déplacer ou renommer.
````markdown
copy C:\users\admin\desktop\dossier1\texte.txt C:\users\admin\desktop\ # copie le fichier texte.txt vers le répertoire "desktop" en utilisant des chemins absolus pour Windows
cp /home/admin/desktop/dossier1/texte.txt /home/admin/desktop/ # copie le fichier texte.txt de dossier1 vers le bureau pour Linux
````
````markdown
move C:\users\admin\desktop\dossier1\texte.txt C:\users\admin\desktop\texte.txt # Déplace le fichier texte.txt sans le renommer sous Windows
move texte.txt texte1.txt # Renomme le fichier texte.txt en texte1.txt sous Windows

mv /home/admin/desktop/dossier1/texte.txt /home/admin/desktop/texte.txt # Déplace le fichier texte.txt sans le renommer sous Linux et macOS
mv texte.txt texte1.txt # Renomme le fichier texte.txt en texte1.txt sous Linux et macOS
````
<span style="color: yellow">rm</span>, ou <span style="color: yellow">del</span> supprimer des éléments.
````markdown
del C:\users\admin\desktop\texte1.txt # supprime le fichier texte1.txt sur Windows
rm /home/admin/desktop/texte1.txt # supprime le fichier texte1.txt sur Linux ou macOS

rmdir repertoire # supprime le répertoire "repertoire" du répertoire courant
````
Pour supprimer un dossier et son contenu, nous devrons utiliser l'option -r de la commande rm sous Linux et macOS. Cette option signifie “recursive”. Cela veut dire que la commande va supprimer tous les fichiers, dossiers et sous-dossiers du répertoire indiqué.
````markdown
rm -r repertoire # supprime le répertoire "repertoire" et son contenu du répertoire courant

rmdir /s C:\users\admin\desktop\dossier1 # supprime le dossier1 et son contenu sur Windows
rm -r /home/admin/desktop/dossier1 # supprime le dossier1 et son contenu sur Linux
````

Lire ou écrire un fichier

Sur Windows, pour modifier un fichier texte, il est possible d'ouvrir le fichier depuis la ligne de commande avec la commande start.
````markdown
start fichier.txt # en utilisant un chemin relatif
start \users\admin\desktop\texte.txt # en utilisant un chemin absolu
````

Vous pouvez afficher le contenu d'un fichier texte avec la commande type.
````markdown
type fichier.txt # affiche des informations sur le fichier
````

Sur Linux ou macOS, un éditeur de texte est déjà installé par défaut : il s'agit de Nano.
````markdown
nano fichier.txt
nano /home/admin/desktop/texte.txt
````
Une fois vos modifications effectuées, vous pouvez enregistrer avec Ctrl+O et sortir de l'éditeur avec Ctrl+X.

Il s'agit d'un éditeur basique. Des éditeurs plus complets sont disponibles au téléchargement gratuitement, comme Emacs, Vim...


<span style="color: yellow">à retenir</span>

La commande <span style="color: yellow">cd</span> permet de se déplacer dans les répertoires, tandis que les commandes <span style="color: yellow">ls</span> (sous Linux et macOS) et <span style="color: yellow">dir</span> (sous Windows) listent le contenu d'un répertoire. La création de dossier se fait avec la commande avec <span style="color: yellow">mkdir</span>.

La création de fichier utilise les commandes <span style="color: yellow">touch</span> (sous Linux et macOS) et <span style="color: yellow">echo</span> (sous Windows).

Les commandes <span style="color: yellow">cp / mv</span> (sous Linux et macOS) et <span style="color: yellow">copy / move</span> permettent respectivement de <span style="color: yellow">copier</span> et de <span style="color: yellow">déplacer</span> ou <span style="color: yellow">renommer</span> des éléments.

Les commandes à utiliser avec précaution <span style="color: yellow">rm</span> (sous Linux et macOS) et <span style="color: yellow">del</span> (sous Windows) permettent de supprimer des éléments.
à finir

<span style="color: lightgreen">d) Commandes utiles</span>

La commande <span style="color: yellow">ping</span> permet de vérifier qu'une machine peut atteindre une autre machine par le réseau local ou par Internet. Cette commande est utile pour savoir si un serveur de base de données est joignable depuis notre poste, par exemple. Cette commande est universelle et fonctionne depuis n'importe quel système d'exploitation.

Il suffit de taper dans le terminal la commande : <span style="color: yellow">ping destination</span>.

<span style="color: yellow">destination</span> peut être une adresse IP ou un nom de domaine.

Résultat de la commande <span style="color: yellow">ping google.fr</span> sur Windows :
````markdown
Envoi d'une requête 'ping' sur google.fr [216.58.201.227] avec 32 octets de données :
Réponse de 216.58.201.227 : octets=32 temps=13 ms TTL=53
Réponse de 216.58.201.227 : octets=32 temps=13 ms TTL=53
Réponse de 216.58.201.227 : octets=32 temps=13 ms TTL=53
Réponse de 216.58.201.227 : octets=32 temps=13 ms TTL=53

Statistiques Ping pour 216.58.201.227:
    Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
Durée approximative des boucles en millisecondes :
    Minimum = 13ms, Maximum = 13ms, Moyenne = 13ms
````

##### <span style="color: yellow">help</span> dans la ligne de commande pour afficher la liste des commandes qui peuvent avoir une aide disponible. Cependant, certaines commandes, comme la commande <span style="color: yellow">ping</span>, n'ont pas la possibilité de fonctionner avec help. C'est pourquoi il existe une syntaxe alternative : <span style="color: yellow">ping /?</span>.
````markdown
help start # permet d'obtenir des informations sur la commande "start"
ping /? # permet d'obtenir des informations sur la commande "ping"
````
Sur Linux, la commande <span style="color: yellow">man</span>, pour manual, regroupe une aide pour beaucoup de commandes. Le fonctionnement est le même que pour Windows.
````markdown
man ping # affiche la page du manuel correspondant à la commande "ping"
````
Depuis votre interface en ligne de commande, il est directement possible de voir l'état de ses cartes réseaux en affichant leur IP, l'adresse IP du sous-réseau ou encore le masque. Cette commande permet de diagnostiquer de potentiels problèmes réseaux, par exemple lorsque le serveur DHCP n'a pas pu correctement délivrer une adresse IP à notre machine.

Sur Windows, il suffit de taper <span style="color: yellow">ipconfig</span> dans le terminal. Sur Linux, la commande <span style="color: yellow">ip a</span> fournit sensiblement les mêmes informations. Quant à macOS, il s'agit de la commande <span style="color: yellow">ipconfig</span>. Pour information, sur beaucoup de distributions plus anciennes de Linux, la commande <span style="color: yellow">ipconfig</span> fonctionnera en lieu et place de <span style="color: yellow">ip a</span>.
````markdown
Configuration IP de Windows


Carte Ethernet Ethernet :

   Suffixe DNS propre à la connexion. . . : home
   Adresse IPv6 de liaison locale. . . . .: fe80::d42f:ee4f:5441:d94b%9
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.1.26
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . : 192.168.1.1

Carte Ethernet VirtualBox Host-Only Network :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::ed08:834e:a48f:78aa%5
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.56.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet VirtualBox Host-Only Network #2 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::1d60:da4b:cac6:4aa8%12
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.99.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet VirtualBox Host-Only Network #3 :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::b135:3622:9646:dbc%34
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.33.1
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . :
````

Sur Linux, la commande <span style="color: yellow">service</span> (ou <span style="color: yellow">systemctl</span>, selon les distributions) permet d'interagir avec les services du système. Il est nécessaire de lancer cette commande avec les privilèges administrateur. Cette commande est importante pour redémarrer des services afin de prendre en compte des modifications effectuées sur un fichier config.
````markdown
sudo service networking restart # cette commande permet de redémarrer le service gérant les connexions réseaux
````

### <span style="color: blue">2. Introduction à Git.</span>

<span style="color: lightgreen">a) Les systèmes de gestion de versions.</span>

Un système de gestion de versions, ou VCS (Version Control System), permet de gérer les versions de nos fichiers en permettant d'accéder à leur historique à un instant T, de sauvegarder notre travail sur un serveur distant ou même de collaborer avec d'autres développeurs.

Il existe plusieurs familles de VCS :

Les VCS locaux (Version Control System) (que nous n'utiliserons pratiquement jamais, puisque nous aurons besoin de stocker une copie de notre base de données de versions sur un serveur distant),

Les CVCS ou CVS centralisés (Centralized Version Control System), qui nous permettent de sauvegarder notre base de données sur un serveur distant et de travailler collaborativement,

Les DCVS, ou CVS distribués (Distributed Version Control System), qui nous permettent d'avoir une copie locale de la base de données en cas de corruption du serveur distant et de pouvoir travailler en local sans connexion.


<span style="color: lightgreen">b) Les avantages de Git.</span>

Git est un système de gestion de version distribué, développé il y a 15 ans pour le projet du noyau Linux. Il a été depuis continuellement amélioré et convient à tous types de projet, même les plus importants.

Sa base de données locale et son système de gestion des instantanés le rendent très performant.

Son système de branches et les trois états de fichiers lui permettent d'être robuste lorsqu'il s'agit de travailler sur un projet, que ce soit seul ou à plusieurs.

Git gère les modifications apportées aux fichiers selon trois états : modifié, validé et indexé.

- Modifié signifie que le fichier a été modifié en local, mais que ses modifications n'ont pas encore été ajoutées à la base de données locale.
  

- Indexé signifie que la version du fichier a été ajoutée au prochain lot de modifications qui seront intégrées à la base de données locale.

    
- Validé signifie que la version du fichier est présente dans la base de données locale.

<span style="color: lightgreen">c) Installation et configuration.</span>

<span style="color: yellow">Git</span> est disponible sous tous les systèmes d'exploitation. Sous Windows, Git met à notre disposition un outil du nom de <span style="color: yellow">GitBash</span> qui nous facilite la vie.

<span style="color: yellow">Git</span> est entièrement personnalisable grâce à la commande <span style="color: yellow">git config</span>, et son option <span style="color: yellow">--global</span> permet de définir la configuration une fois pour tous les projets.

Vérifier que Git est bien disponible et pour afficher sa version :
````markdown
git --version
````
Sous Windows, le résultat devrait ressembler à ceci:
````markdown
git version 2.26.1.windows.1
````
Nous pouvons configurer Git pour qu'il utilise notre nom et notre adresse e-mail:

````markdown
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
````

<span style="color: yellow">git config</span> permet de personnaliser l'installation de Git.

<span style="color: yellow">git config --global --list</span> permet d'afficher facilement la configuration globale de Git. Si on voulait afficher la configuration de notre projet, il suffirait d'omettre l'option <span style="color: yellow">--global</span>.

Comment activer l'auto-correction avec help.autocorrect.

````markdown
git config --global help.autocorrect 1
````


<span style="color: lightgreen">d) Premier projet Git.</span>

Pour pouvoir gérer les versions de nos fichiers, nous avons besoin de travailler dans un dépôt Git. 

Crée un dossier.
````markdown
mkdir exemple-git
````
Allez dans le dossier ainsi crée.
````markdown
cd exemple-git
````

Initialisez le dossier avec la commande <span style="color: yellow">git init</span> afin que <span style="color: yellow">Git</span> en fasse le suivi..

````markdown
git init
````
Crée un fichier README.md.

````markdown
touch README.md
````
Pour créer une nouvelle version de nos fichiers, nous devons ajouter nos fichiers, puis faire un commit. On peut le faire facilement avec les commandes <span style="color: yellow">git add</span> et <span style="color: yellow">git commit</span>.
````markdown
                    Ajouter le fichier README.md
git add README.md

                        Faire un commit.
-m sert pour mettre un message décrivant le commit.
git commit -m"Mon premier commit"
````

Exercice:
Créez un répertoire que vous appellerez exemple-git et rendez-vous dans ce répertoire

Initialisez-y un dépôt Git

Créez un fichier README.md, ajoutez-y du contenu

Ajoutez et commitez ce fichier

Modifiez le fichier

Ajoutez de nouveau ce fichier et effectuez un commit

Correction:
````markdown
mkdir exemple-git && cd $_

git init
echo -e "# Fichier README.md\n\nIl ne contient pas grand choze." > README.md
git add README.md
git commit -m"Mon premier commit"

# On remplace "choze" par "chose" dans le fichier README.md
sed -i "s/choze/chose/" README.md # Sur Linux/Git Bash
# sed -i "" -e "s/choze/chose/" README.md # Sur macOS
git add README.md
git commit -m"Je corrige la faute de frappe"
````






