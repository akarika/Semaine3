#Semaine 3#
----------
Dans cette troiséiéme semaine **GOC** nous aborderons le **C.S.S**

###C.S.S### partie I
-------------
Le CSS (qui signifie Cascading Style Sheets ou feuilles de style en cascade) est un langage utilisé pour définir l'apparence et la forme d'un contenu en HTML.

cela permet d'appliquer le même style à plusieurs éléments HTML sans devoir écrire le code (ex : style="color:red":) pour chacun des éléments

###La balise <link> plus en détails###

Les attributs HTML sont un principe qu’on retrouve en CSS : une paire de mot représente un attribut (un type de comportement) et sa valeur (le comportement exact). Ici la balise <link> prend **trois attributs**.
`type="text/css"` : **le type**, qui permet de donner le format et le langage de données reçues. 
`rel="stylesheeet"` : **l’attribut rel** (pour “relation”) qui indique à quoi servent les données en question.
`href="css/style.css` : **l’attribut href** (pour “hypertext reference”) qui indique ou ce trouvent les données. La valeur du href doit être le chemin sur votre ordinateur/serveur qui mène à votre feuille de style.

####Les selecteurs####

Les sélecteurs sont le coeur du CSS, ils servent comme leur nom l’indique à sélectionner un élément en particulier. Voici la forme que prend un sélecteur:

`sélecteur {
   propriété : attribut;
} `

**Sélecteur** : le nom de la/les balise(s) que vous souhaiter sélectionner.

**Propriété** : la propriété de la balise que sur laquelle vous voulez travailler.

**Attribut** : ce que vous voulez faire de cette propriété.

Prenons un exemple plus parlant. Pour modifier la couleur des paragraphes il suffit donc d'écrire:

`p {
    color : red;
} `

Ici, toutes les balise p verrons la couleur de leur texte passer au rouge grâce à l’attribut color.
Chaque paire de propriété/attribut doit se terminer par un **point-virgule**`;`, ce qui permet de placer une autre paire propriété/attribut. Il est donc possible de faire autant de modifications que l’on souhaite au sein d’un même sélecteur.<br>
Avec ça, vous pouvez sélectionner absolument toutes les balises.<br>
Cependant des fois, on ne veut pas accéder à toutes les balises d’un même type, mais plutôt certaines d’entre elles.<br>Pour ce faire il existe plusieurs solutions, la plus courante consiste à utiliser **l’imbrication des balises**.<br> En effet, en nommant judicieusement son sélecteur on peut **atteindre uniquement les éléments se trouvant à l’intérieur d’autre éléments**.<br> Il suffit de nommer le selecteur en commençant par le plus grand conteneur, d’ajouter un espace, puis d’ajouter le nom d’une balise se trouvant à l’intérieur.
`main section article p {
    color : red;
} `<br>Ici, seuls les paragraphes se trouvant à l'intérieur d’un article, qui eux-mêmes se trouvent dans une section, qui se trouve eux-mêmes dans le main. Pratique ! 
Vous pouvez par ailleurs travailler en même temps sur plusieurs sélecteurs. Par exemple, si vous voulez appliquer les même propriétés/valeurs à un paragraphe et à un titre, il vous suffit de les placer tous les deux, séparés d’une virgule avant l’ouverture des accolades. 
`p {
    font-family: Arial;
    color: blue;
    font-size: 24px;
}`

###faire un commentaire en### **CSS**`<!-- commentaire -->`

####PIXELS ET EM####

Un pixel est un point sur votre écran d'ordinateur.<br> Spécifier la taille de police en pixels, c'est très bien si vous voulez que les visiteurs de votre site web voient exactement la même chose que ce qui est affiché sur votre propre écran.

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


####LES SELECTEURS CSS####

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

Les **ID**, en revanche, sont supers quand vous voulez appliquer un style à **un élément** en particulier.

	<div id="first"></div>
	<div id="second"></div>
	<p id="intro"></p>
	
Dans le CSS, les ID sont identifiés par un dièse #, comme ceci :

`#first {
    height:50px;
}

`#second {
    height:100px;
}

`#intro {
    color:#FF0000
    
les sélecteurs de pseudo-classe

Les sélecteurs de pseudo-classe permettent d'appliquer ce genre de changement de style à notre document HTML. Par exemple, nous avons vu qu'il était possible de changer le style d'un lien pour qu'il ne soit plus en bleu souligné. En utilisant un sélecteur de pseudo-classe, vous pouvez contrôler l'apparence des liens qui n'ont pas été cliqués mais aussi celle des liens que l'utilisateur a seulement survolé avec sa souris, sans cliquer dessus.

selector:pseudo-class_selector {
        property: value;
    }

Voici 3 sélecteurs de pseudo-classe pour les liens (il y en a d'autres). Ils permettent de définir le style pour :

a:link : un lien non cliqué
a:visited : un lien qui a été cliqué
a:hover : un lien survolé par la souris et non cliqué

Le premier enfant
Un autre sélecteur de pseudo-classe utile est first-child. Il est utilisé pour appliquer un style uniquement aux éléments qui sont le premier enfant d'un parent. Par exemple :

   p:first-child {
        color: red;
    }
Cela va mettre tous les paragraphes qui sont les premiers enfants de leurs éléments parents en rouge.

vous pouvez sélectionner n'importe quel enfant d'un élément parent en utilisant le sélecteur de pseudo-classe nth-child. Pour cela, vous ajoutez, entre parenthèses, le numéro de l'enfant que vous souhaitez cibler (ce numéro correspond à la place occupée par cet enfant dans la "descendance" du parent).

Par exemple :

p:nth-child(2) {
    color: red;
}
Cela va attribuer la couleur red à tous les paragraphes qui sont le second enfant de leur parent
Le positionnement 



Maîtriser la position des éléments HTML vous permet d'avoir un contrôle extrêmement précis sur le rendu final de vos pages. Vos <div> ne s'empileront plus les uns sur les autres ! (à moins que vous ne le souhaitiez).


Comme vous l'avez constaté, les boîtes de chaque élément s'étirent sur toute la largeur de la page. C'est pourquoi, jusqu'à maintenant, vos éléments HTML se sont toujours placés les uns au-dessus des autres : par défaut, ils prennent toute la largeur disponible de la page.

Nous pouvons changer cela avec la première propriété de positionnement que nous allons apprendre : la propriété display. Découvrons quatre valeurs de cette propriété.

Block : cela transforme l'élément en boîte de type "bloc" et empêche tout autre élément de se positionner après sur la page. L'élément prend toute la largeur disponible.

Inline-block : cela transforme l'élément en boîte de type "bloc" mais permet à d'autres éléments de se positionner après sur la même ligne.

Inline : cela indique à l'élément de se positionner sur la même ligne que les autres éléments mais sans se formater en tant que "bloc". L'élément prend la largeur dont il a besoin pour s'afficher (pas forcément toute la largeur disponible).

None : l'élément et tout ce qu'il contient disparaissent complètement de la page !

marges

![positions des éléments](https://s3.amazonaws.com/codecademy-blog/assets/ae09140c.png)

La marge externe : margin est l'espace entourant un élément. Plus la marge d'un élément est grande, plus la distance entre cet élément et ceux qui l'entourent sera grande. Nous pouvons ajuster la marge pour rapprocher ou éloigner nos éléments HTML les uns des autres.

La bordure : border est la bordure de chaque élément. C'est ce que l'on rend visible en ajustant la propriété border.

La marge interne : padding est l'espace entre le contenu d'un élément et sa bordure. Nous pouvons ajuster cette valeur avec CSS pour placer les bordures plus ou moins loin du contenu.

Le contenu : content est le contenu de la boîte. par exemple, si on parle d'un élément <p>, le contenu sera le texte du paragraphe.

Vous verrez aussi des abréviations comme TM, TB et TP dans le diagramme. ils correspondent respectivement aux propriétés "top margin", "top border" et "top padding", soit "marge externe du haut", "bordure du haut" et "marge interne du haut". Comme nous le verrons, nous pourrons ajuster individuellement le haut, la droite, la gauche et le bas des propriétés margin, border et padding.


