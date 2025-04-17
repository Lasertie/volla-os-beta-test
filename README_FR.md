# Guide du système d'exploitation Volla

Le système d'exploitation Volla OS et son interface utilisateur spéciale sont continuellement développés. Un aperçu de l'état du développement se trouve sur la plateforme Github, où nous publions le code source du système d'exploitation.

https://github.com/HelloVolla/

Dans le dépôt [volla-os-beta-test](https://github.com/HelloVolla/volla-os-beta-test) vous pourrez également signaler des erreurs et de suivre leur correction.

https://github.com/HelloVolla/volla-os-beta-test/issues

Lorsque vous déverrouillez un téléphone Volla avec Volla OS, vous accédez au Volla Launcher, qui vous permet d'effectuer les fonctions de base de l'appareil, y compris l'ouverture d'applications.

Vous pouvez également atteindre le Volla Launcher par le bouton Accueil au bas de l'affichage ou par un geste de glisser du bas à l'extérieur de l'affichage vers l'intérieur.

Pour complètement enlever la barre de navigation Android, pour le Volla Launcher, il faut aller dans ses paramètres dans le groupe "Affichage et menus" en appuyant sur "Vue plein écran". Vous pouvez accéder aux paramètres Volla Launcher en balayant deux fois à droite, de sorte que les paramètres apparaissent du côté gauche.

L'interface utilisateur Volla comprend deux concepts de base:

1. Tableau de bord avec
    2. champ de texte
    3. Commandes courtes
3. Collection pour
    4. Contacts
    5. Conversations
    6. Nouvelles
    7. Remarques

## Tremplin (Tableau de bord)

Chaque fois que vous appelez le lanceur Volla, il montre le tremplin. L'idée est que, vous écrivez quelque chose et le système reconnaît ce que vous voulez. À cette fin, il fournit des suggestions pour compléter votre entrée ou des fonctions appropriées pour votre entrée.

[Springboard] (screenshot-springboard.jpeg)

Le tremplin supporte les cas d'utilisation suivants :

### Sélection des contacts

Lorsque vous commencez à taper avec le signe @, le système reconnaît que vous voulez écrire un nom et suggère des personnes du carnet d'adresses qui ont étés provisoirement triées par nom. Si vous appuyez sur un nom dans la liste, il sera repris dans le champ texte. Pour pouvoir bénéficier de cette fonction, il faut qu'il y ait des contacts dans votre carnet d'adresses.

En entrant plus de lettres, vous pouvez filtrer la liste des contacts. Ici, le tremplin affiche les noms qui contiennent la séquence de lettres entrée à n'importe quel endroit.

Par exemple, vous pouvez synchroniser le contact avec l'application installée pour synchroniser les carnets d'adresses et les calendriers via le protocole CardDAV et CalDAV.

### Appel
Le système suggère alors d'appeler cette personne. Lorsque vous appuyez sur la suggestion de cette fonctionnalité, le système lance un appel via l'application de téléphonie. Les suggestions pour les fonctions peuvent être reconnues de par leur couleur de fond rouge, contrairement aux suggestion de completion d'entrée.

Vous pouvez reconnaître les suggestions de fonctions par la couleur de fond rouge, contrairement aux suggestions pour compléter votre entrée.

    @Claudia_Sommer

### Messages
Si vous entrez plus de mots au lieu de déclencher un appel, le système suggère que vous pouvez envoyer un message court ou un courriel au contact entré. Appuyez sur la proposition, l'application ouvre actuellement l'application concernée avec un message prérempli, que vous n'avez qu'à envoyer.

    @Claudia_Sommer Tu viens avec nous à l'italien pendant ta pause déjeuner ?
 
Lorsque vous revenez a la ligne après les mots, le système utilise la première ligne pour le sujet d'un courriel. La condition préalable est que vous ayez créé au moins un compte e-mail.

    @Claudia_Sommer Pause déjeuner
    Voulez-vous aller avec nous à l'italien pendant la pause déjeuner ?
    Salutations de Petra

Selon les données stockées pour un contact, le lanceur Volla suggère d'envoyer un message comme SMS, e-mail via le service Signal Messenger.

### Recherche sur le Web
Si vous commencez à taper au lieu d'utiliser un mot au lieu d'un contact, le système suggère de rechercher avec ce mot sur Internet. À cette fin, le système démarre le navigateur avec le mot-clé entré. Par défaut, le lanceur Volla utilise le moteur de recherche [DuckDuckGo] (https://duck.com). Dans les parametres « Moteurs de recherche », vous pouvez également sélectionner [Starpage](https://startpage.com) ou [Metager](https://metager.de).

    Volla

### Note
Si vous entrez plusieurs mots, le système suggère également de créer une note. Ceux-ci peuvent être trouvés après comme une entrée dans les collections pour les notes sur le point rouge à nouveau.

    Volla Phone

Vous pouvez également utiliser les sauts de ligne.

    Téléphone Volla
    Nouvelles fonctions :
    1. mode sécurité
    2. multi boot

### Adresse Web
Lorsque vous entrez une adresse Internet valide, le système suggère de l'ouvrir dans le navigateur.

    Volla.online

### Numéro de téléphone
Si vous saisissez un numéro de téléphone dans le champ texte, le système vous suggère également de déclencher un appel. Comme pour toutes les entrées, un espace à la fin d'un mot ou d'une séquence de nombres est nécessaire pour lancer l'évaluation de l'entrée.

    014323566777


Ensuite, si vous entrez un ou plusieurs mots, le système vous offre d'envoyer un message court, mais pas un courriel.

    014323566777 Bonjour. Petra, comment allez-vous ?

### Adresse électronique

Lorsque vous entrez une adresse e-mail et un texte, le lanceur Volla suggère d'envoyer un courriel.

    hello@volla.online Où puis-je acheter un téléphone Volla?

Si vous revenez à la ligne plusieurs fois, la première ligne est utilisée comme sujet de l'email:

    Bonjour@volla.online Client Volla
    Cher équipe Volla,
    Où puis-je acheter un téléphone Volla?


### Evenement calendrier

Le Volla Launcher reconnais differentes formes de descriptions d'evenements calendriers se constitues de la date, optionellement de l'heure, du titre et optionnellement de sa description. 

	08/12/2022 12:00 Déjeuner avec Peter
	12.08. 16:30 - 17:30 S'entrainer au culb de sport
	6 - 8 pm Dinner avec Paula à Joe's Pizzeria

Si l'heure n'est pas renseigné, le Volla Launcher programmera un evenement sur toute la journée. Erreur seulement la seconde fois pour l'événement. Si la date manque le jour present sera utilisé.

Au lieu d'une date, vous pouvez aussi choisir les jours de la semaine ou une forme courte:

	Tomorrow 10 am video conference avec Paula
	Thursday 14 - 18 o'clock seminaire sur le  vin dans le Ratskeller 

Si vous sautez une ligne, le Volla Launcher utilisera le texte après comme description de l'evenement calendrier. 

Quand vous tappez sur un suguestion pour ajouter un evenement au calendrier, le systeme ouvrirra l'application de calendrier où vous pourrez confirmer l'evenement pour l'envoyer.
	
D'autres fonctions sont prévues

