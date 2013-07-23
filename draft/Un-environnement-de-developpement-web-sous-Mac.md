Un environnement de développement web sous Mac
==============================================


Préambule 0 : Le paradis perdu
------------------------------

Après presque 10 passés à développer sous GNU/Linux, à avoir dompter Apache2, les hosts, le bash, ssh, les clefs publiques, vim, à m'être constitué amoureusement un [répertoire dotfiles](https://github.com/ronanguilloux/dotfiles) plein de trésors rares et autres perles de configuration pour vim, zsh ou que sais-je, mon nouveau job m'impose un nouvel environnement de travail: Mac OS X.
 
Sous GNU/Linux, que j'utilise encore chez moi, mon stack habituel est LAMP et mon environnement de développement quotidien - que je cherche donc à reproduire maintenant sous Mac - est :

* git
* zsh
* vim et une palanquée de plugins vim (merci Pathogen)
* google-chome et une palanquée de plugins indispensables
* quelques outils en ligne de commande liés à PHP (composer, php-cs-fixer), ou pas (ack-grep, tig, diff, rsync, ssh...), que j'utilise tous très fréquemment.

De temps en temps, pour des raisons un peu obscures, il me vient de lancer SublimeText2, ou Meld ou Gitk, alors qu'en fait vim, diff et tig font le job à merveille, et c'est bien pour ça que j'y reviens toujours.


Préambule 1 : Un OS, c'est une opinion
--------------------------------------

Je ne fais pas de GNU/Linux une chapelle, je n'ai pas de gourou, mais j'avoue que pour plein de raisons, c'est encore l'environnement de travail que je préfère et que je conseille. En 2013, à la date de cet article, il devient de plus en plus courant de devoir, en plus du prix de son propre PC, s'abonner à toute sorte de services en ligne liés au Cloud, de devoir débourser quelques euros pour une application simple qui en fait n'est qu'un clickodrome pour des fonctionnalités réellement basiques. Sous Windows 8 comme sous Mac OS X, il faut maintenant un compte (email) en ligne pour pouvoir utiliser son OS à 100%, et on sent bien qu'on devra bientôt payer un abonnement pour utiliser son PC après l'avoir chèrement acheté. Sous GNU/Linux, rien de tel, et même si Ubuntu s'acoquine avec Amazon, on n'en n'est pas encore là. 

Préambule 2 : Les bases les plus basiques
-----------------------------------------

Grand débutant sous Mac, j'ai trouvé toutes les réponses à mes questions essentielles sur le site [DebuterSurMac.com](http://www.debutersurmac.com/tutoriels/accueil.html) : Qu'est-ce qu'un .dmg, comment installer ce qu'on y trouve vers "Mes applications", etc. Ce site est simple les articles essentiels sont vite lus, on s'en sort vite et bien.


Les applications de base
------------------------

**Chrome**  
Safari est un navigateur web sous Mac qui sert à télécharger Chrome.  
Au téléchargemnt, Chrome propose un .dmg (se reporter au préalbule 1) qui s'ouvre dans une feneêtre proposant de glisser-déposer le binaire dans le répertoire Applications. Jusque là, ça va.

