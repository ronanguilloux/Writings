Un environnement de développement web sous Mac
==============================================


Préambule 0 : Le paradis perdu
------------------------------

*où l'on sent poindre une inquiétude : "Ils ont vim, chez Apple ?"*

Après presque 10 passés à développer sous GNU/Linux, à avoir dompté Apache2, les hosts, le bash, ssh, les clefs publiques, vim, à m'être constitué amoureusement un [répertoire dotfiles](https://github.com/ronanguilloux/dotfiles) plein de trésors rares et autres perles de configuration pour mon poste de travail sous Ubuntu, mon nouveau job m'impose maintenant un nouvel environnement de travail: Mac OS X. Tadaaaaa.
 
Sous GNU/Linux, que j'utilise encore chez moi, mon stack habituel est LAMP, quelque fois Go, quelque fois NodeJs, et mon environnement de développement quotidien - que je cherche donc à reproduire maintenant sous Mac - est :

* git
* zsh
* vim et une palanquée de plugins vim (merci Pathogen)
* google-chome et une palanquée de plugins indispensables
* quelques outils en ligne de commande liés à PHP (composer, php-cs-fixer), ou pas (ack-grep, tig, diff, rsync, ssh...), que j'utilise tous assez fréquemment.

De temps en temps, pour des raisons un peu obscures, il me vient de lancer un SublimeText2, ou un Meld ou encore Gitk, alors qu'en fait vim, diff et tig font le job à merveille, et c'est bien pour ça que j'y reviens toujours.

C'est cet environnement de travail que je vais maintenant essayer de retrouver sous Mac, et c'est à cette question que répond cet article ci-dessous, en détail.


Préambule 1 : Un OS, c'est une opinion
--------------------------------------

*où l'inquiétude se confirme : l'auteur voit sa liberté d'utilisateur lui glisser entre les doigts*

Je ne fais pas de GNU/Linux une chapelle, je n'ai pas de gourou, mais j'avoue que pour plein de raisons, c'est encore l'environnement de travail que je préfère et que je conseille chaudement à tous les publics (collègues, parents, école, toussa). 

En 2013 (date de la première version cet article), quand on s'achète un PC, il est devenu courant de devoir s'abonner à toutes sortes de services en ligne liés au Cloud, pour pouvoir utiliser son OS à 100%. Payer ces abonnements, en plus du prix d'achat de son propre PC, licence OS incluse, est devenu une norme. Sous Windows 8 comme sous Mac OS X, il faut maintenant un compte en ligne (impliquant la création d'email @microsoft.com ou @icloud.com) pour pouvoir profiter des services proposées par défaut dans l'OS qu'on a acheté. La plupart de ces abonnements sont aujourd'hui éventuellements gratuits (iCloud, AppStore, Evernote, Dropbox, Wunderlist, et j'en passe) ; à terme ils ont tous vocation à s'imposer comme payants. L'OS dont j'ai acheté la licence est une plateforme, et il y a un (Apple/Google/Microsoft/Ubuntu)-store pour ça.

Sous une Debian (GNU/Linux donc), rien de tel. Même si Ubuntu s'acocquine avec Amazon et développe son propre *Cloud*, on n'en n'est pas encore là. Après l'installation d'une Ubuntu tout fraîche, tout le monde supprime les raccourcis commerciaux présents sur le dock de Unity, et ils ne réapparaitront plus jamais. 

Sous Mac en revanche, l'utilisateur signe dès le  troisième écran d'installation un énorme pacte avec Apple inc. Et quand on vient du Libre et qu'on se veut utilisateur éclairé, ben ça fait juste tout bizarre : en choisissant un OS et en acceptant tous les opt-ins qui nous sont proposés à l'initialisation (Appstore, iCloud et j'en passe), on cautionne de facto toute la politique commerciale de son éditeur. Liberté chérie, tu peux te casser, je couche avec Apple.


Préambule 2 : Les bases les plus basiques
-----------------------------------------

*où l'auteur se dit que bon, c'est pas tout ça, maintenant 'faut bosser avec le Mac*

Une fois ma liste initiale d'applications indispensables établie (chrome - vim - sublimeText3), je me lance dans l'installation. Grand débutant sous Mac, j'ai trouvé toutes les réponses à mes questions essentielles sur le site [DebuterSurMac.com](http://www.debutersurmac.com/tutoriels/accueil.html) : Qu'est-ce qu'un .dmg, comment installer ce qu'on y trouve vers "Mes applications", etc. Ce site est simple les articles essentiels sont vite lus, on s'en sort vite et bien.


Les applications de base
------------------------

**Chrome**  
Safari est un navigateur web sous Mac qui sert à télécharger Chrome.  
Au téléchargement, Chrome propose un .dmg (se reporter au préambule 1) qui s'ouvre dans une fenêtre, proposant visuellement de glisser-déposer soi-même le binaire dans le répertoire Applications. Jusque là, ça va.

