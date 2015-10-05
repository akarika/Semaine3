#Semaine 3#
----------
Dans cette troisième semaine **GOC** nous aborderons le **C.S.S**

###C.S.S### partie I
-------------
Le CSS (qui signifie Cascading Style Sheets ou feuilles de style en cascade) est un langage utilisé pour définir l'apparence et la forme d'un contenu en HTML.

cela permet d'appliquer le même style à plusieurs éléments HTML sans devoir écrire le code (ex : style="color:red":) pour chacun des éléments

###La balise <link> plus en détails###

Les attributs HTML sont un principe qu’on retrouve en CSS : une paire de mots représente un attribut (un type de comportement) et sa valeur (le comportement exact). Ici la balise <link> prend **trois attributs**.
`type="text/css"` : **le type**, qui permet de donner le format et le langage de données reçues. 
`rel="stylesheeet"` : **l’attribut rel** (pour “relation”) qui indique à quoi servent les données en question.
`href="css/style.css` : **l’attribut href** (pour “hypertext reference”) qui indique ou ce trouvent les données. La valeur du href doit être le chemin sur votre ordinateur/serveur qui mène à votre feuille de style.

####Les sélecteurs####

Les sélecteurs sont le coeur du CSS, ils servent comme leur nom l’indique à sélectionner un élément en particulier. Voici la forme que prend un sélecteur:

`sélecteur {
   propriété : attribut;
} `

**Sélecteur** : le nom de la/les balise(s) que vous souhaitez sélectionner.

**Propriété** : la propriété de la balise que sur laquelle vous voulez travailler.

**Attribut** : ce que vous voulez faire de cette propriété.

Prenons un exemple plus parlant. Pour modifier la couleur des paragraphes, il suffit donc d'écrire:

`p {
    color : red;
} `

Ici, toutes les balises p verront la couleur de leur texte passer au rouge grâce à l’attribut color.
Chaque paire de propriétés/attribut doit se terminer par un **point-virgule**`;`, ce qui permet de placer une autre paire propriété/attribut. Il est donc possible de faire autant de modifications que l’on souhaite au sein d’un même sélecteur.<br>
Avec ça, vous pouvez sélectionner absolument toutes les balises.<br>
Cependant des fois, on ne veut pas accéder à toutes les balises d’un même type, mais plutôt certaines d’entre elles.<br>pour ce faire il existe plusieurs solutions, la plus courante consiste à utiliser **l’imbrication des balises**.<br> En effet, en nommant judicieusement son sélecteur on peut **atteindre uniquement les éléments se trouvant à l’intérieur d’autres éléments**.<br> Il suffit de nommer le sélecteur en commençant par le plus grand conteneur, d’ajouter un espace, puis d’ajouter le nom d’une balise se trouvant à l’intérieur.
`main section article p {
    color : red;
} `<br>Ici, seuls les paragraphes se trouvant à l'intérieur d’un article, qui eux-mêmes se trouvent dans une section, qui se trouve eux-mêmes dans le main. Pratique ! 
Vous pouvez par ailleurs travailler en même temps sur plusieurs sélecteurs. Par exemple, si vous voulez appliquer les mêmes propriétés/valeurs à un paragraphe et à un titre, il vous suffit de les placer tous les deux, séparés d’une virgule avant l’ouverture des accolades. 
`p {
    font-family: Arial;
    color: blue;
    font-size: 24px;
}`

###faire un commentaire en### **CSS**`<!-- commentaire -->`

####PIXELS ET EM####

Un pixel est un point sur votre écran d'ordinateur.<br> spécifier la taille de police en pixels, c'est très bien si vous voulez que les visiteurs de votre site web voient exactement la même chose que ce qui est affiché sur votre propre écran.

L'unité de mesure **em** est une mesure relative : un **em** est égal à la taille de police par **défaut de l'écran utilisé**.<br> C'est donc parfait pour les smartphones.<br>Une taille de police en em dit seulement : "Hey, 1em, c'est la taille de police utilisée normalement ; la valeur 2em correspond à une taille de police deux fois plus grande ; la valeur 0.5em correspond à une taille de police deux fois plus petite !".

####Les polices####

**Serif** : dans ce type de police, les extrémités des lettres ont des extensions. La Garamond est une police serif.

**Sans-serif** : c'est une police sans extensions. L'Arial et la Verdana sont des polices sans-serif.

**Cursive** : c'est une police qui ressemble à une écriture manuscrite.

####Couleur d'arrière-plan, hauteur et largeur####

La couleur d'arrière-plan du bloc `background-color`, pour laquelle vous choisissez une valeur hexadécimale.<br>
La hauteur du bloc `height` que vous mesurez en pixels.<br>
La largeur du bloc ` width` en pixels également.<br>
La propriété `border` peut prendre plusieurs valeurs. Par exemple, pour afficher une bordure de 2 pixels, continue et rouge, il suffit d'écrire :<br>
`selector {
    border:2px solid red;
}`
<br>
Mais les liens ont une autre propriété : `text-decoration` qui permet de modifier votre lien pour qu'il soit un peu plus beau<br>

**boutons**<br>
border-style peut être de n'importe quel type (dashed, solid, etc.) et de n'importe quelle épaisseur (border-width) (2 pixels, c'est bien)<br>

-----------------------------------
###C.S.S### partie II
----------------------


####LES SÉLECTEURS CSS####

 **tous** les éléments **HTML** peuvent être utilisés comme **sélecteurs CSS** ! Vous pouvez donc modifier des balises ```<ul>```, `<table>` et même **l'intégralité** de ce qui se trouve dans `<body>` en utilisant respectivement comme sélecteurs **ul**, **table** ou **body**.<br> Vous savez qu'il est possible d'imbriquer des éléments HTML les uns à l'intérieur des autres, comme ceci :
 
	* {
 		<div>
        	<div>
            	<p>J'aime les tacos !</p> 

div div p {
        /*votre code CSS!*/
    }
    `
    y a aussi un sélecteur très spécial qui permet d'appliquer des styles CSS à tous les éléments de la page : le sélecteur *. Par exemple, si vous tapez :
    
	* {
    	border: 2px solid black;
    	}
    	
####Classes et ID####

   	
Les classes sont utiles quand vous avez besoin d'appliquer le même style à **plusieurs éléments** HTML différents.

	
	<div class="square"></div>
	<img class="square"/>
	<td class="square"></td>

Dans le CSS, les classes sont identifiées par un point . comme cela :

	.square {
    height: 100px;
    width: 100px;
	}`

Les **ID**, en revanche, sont super quand vous voulez appliquer un style à **un élément** en particulier.

	<div id="first"></div>
	<div id="second"></div>
	<p id="intro"></p>
	
Dans le CSS, les ID sont identifiés par un dièse #, comme ceci :

	#first {
    height:50px;
	}

	#second {
    height:100px;
	}
	#intro {
    color:#FF0000
    }
    
####les sélecteurs de pseudo-classe####

Les sélecteurs de pseudo-classe permettent d'appliquer ce genre de changement de style à notre document HTML. En utilisant un sélecteur de pseudo-classe, vous pouvez contrôler **l'apparence des liens qui n'ont pas été cliqués**, mais aussi celle des liens que l'utilisateur a seulement **survolé avec sa souris, sans cliquer dessus**.

	selector:pseudo-class_selector {
		property: value;
    	}

Voici 3 sélecteurs de pseudo-classe pour les liens (il y en a d'autres). Ils permettent de définir le style pour :

`link` : un lien non cliqué
`visited` : un lien qui a été cliqué
`hover` : un lien survolé par la souris et non cliqué

**Le premier enfant**

Un autre sélecteur de pseudo-classe utile est `first-child`. Il est utilisé pour appliquer un **style uniquement** aux éléments qui sont le **premier enfant d'un parent**. Par exemple :
`
   p:first-child {
        color: red;
    }
    `
Cela va mettre tous les **paragraphes** qui sont les **premiers enfants de leurs éléments parents en rouge**.

vous pouvez **sélectionner** n'importe quel enfant d'un **élément parent** en utilisant le sélecteur de pseudo-classe `nth-child`. Pour cela, vous ajoutez, **entre parenthèses**, le **numéro de l'enfant** que vous souhaitez cibler (ce numéro correspond à la place occupée par cet enfant dans la "descendance" du parent).

`
p:nth-child(2) {
    color: red;
}
`
Cela va **attribuer** la couleur **red** à tous les paragraphes qui sont le **second enfant de leur parent**


--------------
###C.S.S### partie III
-----------


####Le positionnement#### 



Maitriser la **position des éléments HTML** vous permet d'avoir un **contrôle extrêmement précis** sur le rendu final de vos pages. Vos `<div> `ne s'empileront plus les uns sur les autres ! (à moins que vous ne le souhaitiez).


C'est pourquoi, jusqu'à maintenant, vos **éléments HTML** se sont toujours placés **les uns au-dessus des autres** : **par défaut**, ils prennent toute la **largeur** disponible de la page.

Nous pouvons changer cela la propriété **display**. Découvrons quatre valeurs de cette propriété.

`Block` : cela transforme l'élément en boite de type "bloc" et empêche tout autre élément de se positionner après sur la page. L'élément prend toute la largeur disponible.

`Inline-block` : cela transforme l'élément en boite de type "bloc", mais permet à d'autres éléments de se positionner après sur la même ligne.

`Inline` : cela indique à l'élément de se positionner sur la même ligne que les autres éléments, mais sans se formater en tant que "bloc". L'élément prend la largeur dont il a besoin pour s'afficher (pas forcément toute la largeur disponible).

`None` : l'élément et tout ce qu'il contient disparaissent complètement de la page !

marges

![ici les différents types](https://camo.githubusercontent.com/3134f9555fc0adc294dc9b639500d61be6faca3d/687474703a2f2f342e62702e626c6f6773706f742e636f6d2f2d5469774f69786c6f6f4a6b2f55345579456e765f5870492f41414141414141414346732f4e75754c7a3249766f5a342f73313630302f6373732d646973706c61792d626c6f636b2d76732d696e6c696e652d626c6f636b2e706e67)

####Les marges####

**La marge externe** : `margin` est l'espace entourant un élément. Plus la marge d'un élément est grande, plus la distance entre cet élément et ceux qui l'entourent sera grande. Nous pouvons ajuster la marge pour rapprocher ou éloigner nos éléments HTML les uns des autres.

**La bordure** : `border` est la bordure de chaque élément. C'est ce que l'on rend visible en ajustant la propriété border.

**La marge interne** : `padding` est l'espace entre le contenu d'un élément et sa bordure. Nous pouvons ajuster cette valeur avec CSS pour placer les bordures plus ou moins loin du contenu.

**Le contenu** : content est le contenu de la boite. Par exemple, si on parle d'un élément `<p>`, le contenu sera le texte du paragraphe.

Vous verrez aussi des abréviations comme TM, TB et TP dans le diagramme. ils correspondent respectivement aux propriétés "top margin", "top border" et "top padding", soit "marge externe du haut", "bordure du haut" et "marge interne du haut". Comme nous le verrons, nous pourrons ajuster individuellement le haut, la droite, la gauche et le bas des propriétés margin, border et padding.

![positions des éléments](https://s3.amazonaws.com/codecademy-blog/assets/ae09140c.png)


####Positionnement flottant####

Une manière de faire est d'utiliser des éléments flottants floats. Quand vous faites flotter un élément sur la page, vous dites à la page Web : "Je vais te dire où mettre cet élément, mais tu dois le faire flotter au-dessus des autres éléments." Cela signifie que si vous avez plusieurs éléments, tous flottants, ils savent tous que les autres sont là et ils ne se recouvrent pas les uns les autres.


	div {
		height: 300px;
		width: 100px;
		border: 2px solid black;
		border-radius: 5px;
		background-color: #308014;
		float:left;
	
	}
	

![float](http://fr.html.net/tutorials/css/figure016.gif)

Si vous dites à un élément clear: left (libérer la gauche), il se déplacera immédiatement en dessous de tout élément flottant sur le côté gauche de la page ; il peut également libérer des éléments sur la droite (right). Si vous lui dites clear: both, il libèrera de l'espace aux éléments flottants à gauche et à droite !

`
element {
    clear: /*right (droite), left (gauche), ou both (les deux)*/
}
`


####Position relative, absolue et fixe####



####La position relative####

La position relative (position:relative) permet de décaler un élément par rapport à **une position de référence**: celle qu'il avait dans le flux. Les éléments qui le suivent et le précèdent ne sont pas influencés par ce décalage puisqu'ils considèrent que l'élément est toujours dans le flux à sa position initiale. En pratique, ce comportement est rarement recherché bien qu'il puisse s'avérer utile dans certains cas.

Attribuer à un élément une position relative peut par contre être pratique, voire indispensable, dans d'autres situations dont les plus courantes sont sans nul doute les suivantes:

Servir de référent à un élément enfant positionné en absolu (rappelons qu'un élément positionné absolument grâce aux propriétés top, left, … le fera par rapport à la fenêtre du navigateur à défaut d'avoir un parent lui-même positionné)
Bénéficier de la possibilité d'utiliser la propriété **z-index** pour gérer des superpositions d'éléments (propriété inopérante pour des éléments du flux)
La position absolue

####La position absolue####

 (position:absolute) permets de ne pas dépendre de **l'ordre dans lequel les éléments HTML sont déclarés dans le code**, contrairement aux flottants que nous verrons plus tard.

La position absolue s'affranchit définitivement du cordon liant jusqu'alors intimement contenu et présentation. L'élément étant totalement extrait du flux, il ne dépend plus du tout des éléments qui le côtoient. Il faut voir le positionnement absolu comme étant une méthode radicale (mais puissante) qui retire tout à fait un élément du flux: il n'existe pour ainsi dire plus aux yeux des éléments qui, eux, restent dans le flux.

Rappelons un point important concernant ce mode de positionnement : un élément positionné en absolu se réfère non pas à son parent direct, mais au premier ancêtre positionné qu'il rencontre.

L'élément, n'étant plus dans le flux naturel, perd une de ses caractéristiques majeures qui est celle de recouvrir la totalité de la largeur disponible de l'élément parent.

Il est capital de noter qu'un élément bénéficiant d'une position absolue ne bougera pas de sa position initiale tant que l'une des propriétés top, bottom, left ou right n'a pas été précisée; il s'agit d'ailleurs là d'un comportement appliquable à toutes les positions.

####La position fixe####

Le positionnement fixe (position:fixed) s'apparente au positionnement absolu, à l'exception des points suivants:

Lorsque le positionnement est précisé (top, right, …), l'élément est toujours positionné par rapport à la fenêtre du navigateur
L'élément est fixé à un endroit et ne pourra se mouvoir, même lors de la présence d'une barre de défilement. En d'autres termes, la position intiale est fixée au chargement de la page, le fait qu'une éventuelle scrollbar puisse être utilisée n'a aucune influence sur le positionnement de l'élément: il ne bouge plus de la position initialement définie.
La position statique

La position statique (position:static) correspond simplement à la valeur par défaut d'un élément du flux. Il n'y a que peu d'intérêt à la préciser, si ce n'est dans le but de rétablir dans le flux un élément en particulier parmi une série qui serait positionnée hors du flux.

![](http://i.stack.imgur.com/wA8sA.gif)

**Le positionnement flottant** (avec la propriété, float) est l'un des plus utilisés à l'heure actuelle. Il permet par exemple de placer un menu à gauche ou à droite de la page. Néanmoins, cette propriété n'a pas été initialement conçue pour cela et il est préférable, si possible, d'éviter cette technique.

**Le positionnement inline-block** consiste à affecter un type inline-block à nos éléments grâce à la propriété display. Ils se comporteront comme des inlines (placement de gauche à droite), mais pourront être redimensionnés comme des blocs (avec width et height). Cette technique est à préférer au positionnement flottant.

**Le positionnement absolu** permet de placer un élément où l'on souhaite sur la page, au pixel près.

**Le positionnement fixe** est identique au positionnement absolu, mais l'élément restera toujours visible même si on descend plus bas dans la page.

**Le positionnement relatif** permet de décaler un bloc par rapport à sa position normale.
Un élément A positionné en absolu à l'intérieur d'un autre élément B (lui-même positionné en absolu, fixe ou relatif) se positionnera par rapport à l'élément B, et non par rapport au coin en haut à gauche de la page.

Z-index


![](http://jean.yard.pagesperso-orange.fr/sitelycee/cours/html5css3/lib/NouvelElement226.png)
