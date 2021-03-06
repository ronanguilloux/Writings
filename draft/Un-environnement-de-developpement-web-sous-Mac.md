---
published: false
---

Un environnement de développement web sous Mac
==============================================


Préambule 0 : Le paradis perdu
------------------------------

*où l'on sent poindre une inquiétude : "Ils ont vim, chez Apple ?"*

Après presque 10 ans passés à développer sous GNU/Linux, à avoir dompté Apache2, les hosts, le bash, ssh, les clefs publiques, vim, à m'être constitué amoureusement un [répertoire dotfiles](https://github.com/ronanguilloux/dotfiles) plein de trésors rares et de perles de configuration pour mon poste de travail sous Ubuntu, mon nouveau job m'impose maintenant un nouvel environnement de travail: Mac OS X. Tadaaaaa.
 
Sous GNU/Linux (que j'utilise encore chez moi) mon stack habituel est LAMP, quelque fois Go, quelque fois NodeJs, et mon environnement de développement quotidien - que je cherche donc à reproduire maintenant sous Mac - est donc :

* git
* zsh
* vim et une palanquée de plugins vim (merci Pathogen)
* google-chome et une palanquée de plugins indispensables
* quelques outils en ligne de commande liés à PHP (composer, php-cs-fixer), ou pas (ack-grep, tig, diff, rsync, ssh...), que j'utilise tous assez fréquemment.

De temps en temps, pour des raisons un peu obscures, il me vient de lancer un SublimeText2, ou un Meld ou encore Gitk, alors qu'en fait vim, diff et tig font le job à merveille, et c'est bien pour ça que j'y reviens toujours.

C'est cet environnement de travail que je vais maintenant essayer de retrouver sous Mac, et c'est à cette question que répond cet article ci-dessous, en détail.

La deuxième question à laquelle répond cet article est : ["Is OS X for WEB developers?"](http://zachholman.com/2011/03/osx-isnt-for-developers)

Préambule 1 : Un OS, c'est une opinion
--------------------------------------

*où l'inquiétude se confirme : l'auteur voit sa liberté d'utilisateur lui glisser entre les doigts*

Je ne fais pas de GNU/Linux une chapelle, je n'ai pas de gourou, mais j'avoue que pour plein de raisons, c'est encore l'environnement de travail que je préfère et que je conseille chaudement à tous les publics (collègues, parents, école, toussa). 

En 2013 (date de la première version cet article), quand on s'achète un PC dans un magasin et qu'on le ramène chez soi, il est devenu courant de devoir ensuite s'abonner à toutes sortes de services en ligne, liés au Cloud, pour pouvoir utiliser son OS à 100%. Payer ces abonnements, en plus du prix d'achat de son propre PC, licence OS incluse, est devenu une norme. Sous Windows 8 comme sous Mac OS X, il faut maintenant un compte en ligne (impliquant la création d'email @microsoft.com ou @icloud.com) pour pouvoir profiter des services proposés par défaut dans l'OS qu'on a acheté. La plupart de ces abonnements sont aujourd'hui éventuellement gratuits (iCloud, AppStore, Evernote, Dropbox, Wunderlist, et j'en passe) ; à terme ils ont tous vocation à s'imposer comme payants. L'OS dont j'ai acheté la licence est une plateforme, et il y a un (Apple/Google/Microsoft/Ubuntu)-store pour ça.

Sous une Debian (GNU/Linux donc), rien de tel. Même si Ubuntu s'acoquine avec Amazon et développe son propre *Cloud*, on n'en n'est pas encore là. Après l'installation d'une Ubuntu tout fraîche, tout le monde [supprime les raccourcis commerciaux](http://goo.gl/wTwLW) présents sur la barre de liens d'Unity, et ils ne réapparaitront plus jamais.

Sous Mac en revanche, l'utilisateur signe dès le troisième écran d'installation un énorme pacte avec Apple Inc. Et quand on vient du Libre et qu'on se veut utilisateur éclairé, ben ça fait juste tout bizarre : en choisissant un OS et en acceptant tous les opt-ins qui nous sont proposés à l'initialisation (Appstore, iCloud et j'en passe), on cautionne de facto toute la politique commerciale de son éditeur. Liberté chérie, tu peux te casser, je couche avec Apple.


Préambule 2 : Les bases les plus basiques
-----------------------------------------

*où l'auteur se dit que bon, c'est pas tout ça, maintenant 'faut bosser avec le Mac*

Une fois ma liste initiale d'applications indispensables établie (chrome - vim - SublimeText3, etc.), je me lance dans l'installation, en commençant par parcourir les sites web des éditeurs de ces différents logiciels, souvent déjà utilisés sous Ubuntu. Je me retrouve avec mes premiers .dmg dans mon répertoire "Téléchargements", sans trop savoir qu'en faire. Double-cliquer ? Jeune débutant sous Mac, j'ai trouvé toutes les réponses à mes questions essentielles sur le site [DebuterSurMac.com](http://www.debutersurmac.com/tutoriels/accueil.html) : Qu'est-ce qu'un .dmg, comment installer ce qu'on y trouve vers "Mes applications", etc. Ce site est simple, les articles essentiels sont vite lus, on s'en sort vite et bien.


1 - Les applications de base
----------------------------

Les **.dmg** téléchargés sur les sites des différents éditeurs de logiciels (se reporter au préambule 2) aterrissent donc dans le dossier Téléchargements et s'ouvrent au clic dans une nouvelle fenêtre du Finder pour afficher le contenu de cette archive, proposant même quelquefois visuellement de glisser-déposer soi-même le binaire dans le répertoire Applications. Cette démarche vaut pour 90% des cas, et sinon il faut la faire à la main si nécessaire. Le "disque" .dmg peut ensuite être éjecté. L'application est installée, pour de bon.

**Les .dmg téléchargées et installées alla mano**

* Google-Chrome
* Google Drive (proposée sur drive.google.com)
* [iTerm2](http://www.iterm2.com) version "test" (très bon émulateur de terminal)
* Transmission (client Bittorrent)
* VLC
* SublimeText3
* Github (proposée sur mac.github.com)
* Virtualbox
* Vagrant
* Spotify
* 
Pour iTerm2, je recommande cet article : [Working Effectively With iTerm2](http://goo.gl/Ipb4Wn).
Pour les utilisateur de clavier mac déporté, afin de profiter du pavé numérique, 
il faut sélectionner "xterm with numeric keypad" dans les configurations de clavier (preset) dans prefs->profiles->keys

Assez vite on tombe sur des sites d'applications expliquant qu'il faut allez sur l'Appstore pour télécharger l'appli désirée. L'Appstore ouvert dans Mac OS X se révèle très proche dans son fonctionnement de la logithèque d'Ubuntu ou du Google Play d'Android : on y trouve "Les apps les + téléchargées", "Par thématiques", "Les gratuits", etc. OK, fastoche donc.

**Les applications installées via AppStore**

* QuickHub (OS X dedicated Github tool)
* The Unarchiver
* TweetDeck
* Wunderlist
* Evernote

Bref que des petits logiciels pas essentiel pour la prod, en fait.


2 - Command Line Tools for Xcode
--------------------------------

Je cite http://pym.me/posts/installer-et-configurer-un-environnement-de-developpement-ruby-sur-mac-os-x :

>L'étape indispensable (et susceptible de prendre un peu de temps) est l'installation des Command Line Tools for Xcode. C'est un gros package contenant l'ensemble des outils qui vont nous être utiles pour la suite.

>This package enables UNIX-style development via Terminal by installing command line developer tools, as well as Mac OS X SDK frameworks and headers. Many useful tools are included, such as the Apple LLVM compiler, linker, and Make. If you use Xcode, these tools are also embedded within the Xcode IDE, and can be installed on your system using the Downloads preferences pane within Xcode 4.5.
À noter que pour peu que vous ayez déjà développé sur Mac, il y a de grandes chances pour que vous ayez déjà installé la suite.

J'ai donc suivi les consignes : Installer Xcode (via l'Appstore, près d'un Giga o_O), aller dans Préférences > Téléchargements, installer les Command Line Tools (118,5 Mo).

On verra plus loin qu'en sautant cette étape on se retrouve avec des warnings dans les installations avec `brew` (cf. le point 4), donc autant ne pas faire l'impasse.


3 - ZSH
-------
Zsh, c'est le shell des gens qui utilisent tout le temps leur shell. Il est installé par défaut dans Mac. On le tweak ici avec l'excellent [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh), que j'ai longtemps utilisé sous Ubuntu:

``` bash
$ curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
```
Pas encore réussi à installer correctement les fonts pour [Powerline](https://github.com/jeremyFreeAgent/oh-my-zsh-powerline-theme), ça attendra


4 - HomeBrew
------------

Installation de `brew`:

``` bash
$ ruby -e "$(curl -fsSkL raw.github.com/mxcl/homebrew/go)"
```

Les outils installés:

``` bash
brew install the_silver_searcher wget tree tig
```

`the_silver_searcher`se veut encore mieux que ack, je ne l'ai découvert qu'après coup, [il est documenté ici](https://github.com/ggreer/the_silver_searcher), "a code-searching tool similar to ack, but faster".

Je n'ai pas installé git via brew (version 1.8.3) puisque la 1.8.1 a été installé avec l'appli mac de Github (cf. plus haut)

L'autocomplétion de `brew` dans `zsh`est vraiment utile, [l'installation](https://github.com/mxcl/homebrew/wiki/Tips-N%27-Tricks#zsh) est documentée ici 


5 - Vagrant : Mise en place
---------------------------

Vagrant, c'est ça :

``` bash
$ vagrant box add lucid32 http://files.vagrantup.com/lucid32.box
$ vagrant init lucid32
$ vagrant up
```

Plus un simple accès SSH pour rentrer dans la machine virtualisée 

``` bash
$ vagrant ssh
...
vagrant@vagrantup:~$
```

Ce paragraphe décrit comme nous allons résoudre la plus grande partie notre problème  : l'environnement de développement \*AMP sous MAC.

Le but est ici d'installer quelque chose de mieux que [MAMP](http://fr.wikipedia.org/wiki/MAMP), et même mieux qu'un simple [LAMP](http://fr.wikipedia.org/wiki/LAMP) local sous GNU/Linux, pour trouver à la place un moyen de monter rapidement **plusieurs** machines virtuelles, une par environnement de production (une par projet, si chaque projet correspond à un serveur dédié différent). eE but est d'avoir, sur chaque projet en local, une configuration exactement similaire à l'environnement de production de ce projet. Le même OS dans la même version, la même version d'Apache, de PH, la même version du moteur de base de données, les mêmes librairires, etc.

Dis comme ça ça semble bien compliqué, mais il y a des outils de virtualisation qui font ça les doigts dans le nez.

C'est notamment ce que fait [Vagrant](http://www.vagrantup.com/) et c'est simplement bluffant.


On trouvera [une liste de boxes (machines virtuelles) pour Vagrant ici](http://www.vagrantbox.es/) : ArchLinux, Debian, Ubuntu de toutes versions, et même Windows Server, tout y est ou presque.

C'est vraiment simple : En trois lignes de shell c'est monté. Un petit fichier bootstrap.sh permet d'installer et de configurer ce dont on a besoin. Un répertoire /vagrant à la racine du serveur virtuel est partagé avec l'hote (l'OS de MAC), c'est donc là qu'on peut éditer son code source. On peut donc travailler directement depuis Mac, sans avoir à "rentrer" dans la machien virtuelle en permanence.

**My beloved GUI EDI Vs my PHP Quality Assurance Toolchain**

C'est à la fois un gros gain et un problème, quand on fait le choix systématique d'un [environnement de développement intégré](http://fr.wikipedia.org/wiki/Environnement_de_d%C3%A9veloppement_int%C3%A9gr%C3%A9) (comprenez : un éditeur de code source) avec une jolie [interface graphique](http://fr.wikipedia.org/wiki/Interface_graphique), par exemple SublimeText3. Pourquoi ? Parce que ce type d'IDE graphique, qui donc n'est pas directement sur l'OS virtualisé va habituellement gagner à utiliser des plugins tiers utilisant eux-mêmes des extensions de PHP ou des librairies écrites en PHP : **[phpunit, phpmd, phpcs, php-cs-fixer, etc.](http://phpqatools.org/)** pour améliorer l'expérience d'écriture du code. A cause de notre IDE préféré tout beau et tout clicable, il faudra donc installer tout ça via pear (par exemple) sur l'OS hôte (MAC) et non sur le serveur virtualisé. 

Donc en fait on se retrouve à maintenir une version de PHP sur Mac et une autre dans la box vagrant. Grrrrrrr.

L'alernative est simple mais radicale : ouvrir avec `vagrant ssh` une session SSH sur la machine virtuelle, et tout faire sous Vim sur cette machine. Bref, dans mon cas, travailler exactement comme sur une machine hôte GNU/Linux. Moi ça me dérangerai pas, mais ça peut devenir bloquant s'il faut proposer cette solution à toute l'équipe de production qui veut justement se mettre à Vagrant :-/

J'en suis là, je vous raconterai à la longue si c'est point bloquant


X - Annexes
-----------

**OpenSource fonts**

J'ai échoué pour l'instant à installer Powerline (peut importe en fait) par contre ça m'a fait découvrir [Powerline-Fonts](https://github.com/Lokaltog/powerline-fonts), un symathique dépot de fonts libres adaptées à l'édition de code.
