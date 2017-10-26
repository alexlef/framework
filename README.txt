Framework réalisé par :
	Lefevre Alexandre
	Aubert Enzo
	Sipp Hugo

Installation framework sous forme CSS :

	_Récuperer le dossier CSS, l'ajouter a votre projet.
	_Dans le fichier html ne pas oublier de signaler son utilisation :
			<link rel="stylesheet" href="css/all.css">
			
Si vous souhaitez modifier le css, il vous suffit de créer un nouveau fichier .css et de modifier les classes voulu dedans.
		
		
Installation framework sous forme SCSS :

	_Créer votre propre fichier .scss
	_faites un :
		@import "all"
	_redefinnissez vos classes comme vouls souhaitez gràce mixin fournies : certain élèments ont déja une valeurs attribué pour vous éviter à devoir les refaires.
	_Vous pouvez modifier directement certains attributs depuis le fichier _param.scss, simplement en enlevant le commentaire 
	_Créez votre fihier .css avec cette commande (depuis le repertoire supérieur) :
		sass --watch scss:css
	
Listes de toutes les mixin ou paramètres présent :

	Les mixin :
	
	Pour les boutons :
		struct($width:inherit,$br:none,$display:inline-block,$margbot:2%,$margtop:2%) : définit la structure
		txt($fs:150%,$txtd:none,$txtalign:center,$color:white) : définit la structure du texte
		style($border:none,$padd:2% 2%,$cursor:pointer,$bshad:none) : définit le style
	
	Pour la grille :
		grille($width:100%,$padd:0 0 0 0,$height:auto) : définit les propriétés de la grille 
		ligne($witdh:100%,$display:flex, $flex-dir:row) : définit les propriétés d'une ligne
		posdim ($nb-col,$col,$marg,$flex-grow:0,$flex-shrink:1,$center:auto) : définit le nombre de colonne de la ligne, et la taille de la colonne
		offset ($nb-col,$col,$marg,$margin:auto) : definit l'offset d ela colonne actuelle
		
	Les param :
	
		Les BOUTONS 
		Les ALERTES
		Les TITRES
		La NAVBAR
		Les ALERTES
	
Il y a deux exemples fournies qui utilisent le framework :	

	Exemple.html utilise le css :
		exempleNonSass
	C'est a dire qu'il utilise ce css qui prend le dessus face a celui du framework afin de modifié certaines valeurs du framework.

	Accueil.html utilise sass : 
	C'est a dire qu'il import le fichier "all" et défini lui même ses classes par la suite.

