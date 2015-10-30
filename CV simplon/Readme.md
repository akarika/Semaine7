#COMMENT FAIT-ON POUR CRÉER DES SITES WEB ?#



Le Web a été inventé par Tim Berners-Lee au début des années 1990.</br>
Pour créer des sites web, on utilise deux langages informatiques :</br>
1.HTML : permet d'écrire et organiser le contenu de la page (paragraphes, titres…) ;</br>
2.CSS : permet de mettre en forme la page (couleur, taille…).</br>
Il y a eu plusieurs versions des langages HTML et CSS. Les dernières versions sont HTML5 et CSS3.</br>
Le navigateur web est un programme qui permet d'afficher des sites web. Il lit les langages HTML et CSS pour savoir ce qu'il doit afficher.</br>
Il existe de nombreux navigateurs web différents : Google Chrome, Mozilla Firefox, Internet Explorer, Safari, Opera… Chacun affiche un site web de manière légèrement différente des autres navigateurs.</br>
Dans ce cours, nous allons apprendre à utiliser les langages HTML et CSS. Nous travaillerons dans un programme appelé « éditeur de texte » (Notepad++, jEdit, vim…).</br>

###VOTRE PREMIÈRE PAGE WEB EN HTML###

On utilise l'éditeur de texte (Notepad++, jEdit, vim…) pour créer un fichier ayant l'extension .html (par exemple : test.html). Ce sera notre page web.</br>
Ce fichier peut être ouvert dans le navigateur web simplement en faisant un double-clic dessus.</br>
À l'intérieur du fichier, nous écrirons le contenu de notre page, accompagné de balises HTML.</br>
Les balises peuvent avoir plusieurs formes :
`<balise> </balise>` : elles s'ouvrent et se ferment pour délimiter le contenu (début et fin d'un titre, par exemple).</br>
`<balise />` : balises orphelines (on ne les insère qu'en un seul exemplaire), elles permettent d'insérer un élément à un endroit précis (par exemple une image).</br>
Les balises sont parfois accompagnées d'attributs pour donner des indications supplémentaires `(exemple : <image nom="photo.jpg" />`).</br>
Une page web est constituée de deux sections principales : un en-tête `<head>` et un corps `<body>`.</br>
On peut afficher le code source de n'importe quelle page web en faisant un clic droit puis en sélectionnant Afficher le code source de la page.</br>

###ORGANISER SON TEXTE###

Le HTML comporte de nombreuses balises qui nous permettent d'organiser le texte de notre page. Ces balises donnent des indications comme « Ceci est un paragraphe », « Ceci est un titre », etc.</br>
Les paragraphes sont définis par la balise `<p> </p>` et les sauts de ligne par la balise `<br />`.</br>
Il existe six niveaux de titre, de `<h1>` `</h1>` à `<h6>` `</h6>`, à utiliser selon l'importance du titre.</br>
On peut mettre en valeur certains mots avec les balises `<strong>`, `<em>` et `<mark>`.</br>
Pour créer des listes, on doit utiliser la balise `<ul>` (liste à puces, non ordonnée) ou `<ol>` (liste ordonnée). À l'intérieur, on insère les éléments avec une balise `<li>` pour chaque item.</br>


###CRÉER DES LIENS###

Si votre fichier cible est placé dans un dossier qui se trouve « plus haut » dans l'arborescence, il faut écrire deux points comme ceci :</br>

`<a href="../page2.html">`

Un lien pour envoyer un e-mail

Si vous voulez que vos visiteurs puissent vous envoyer un e-mail, vous pouvez utiliser des liens de type `mailto`.</br> Rien ne change au niveau de la balise, vous devez simplement modifier la valeur de l'attribut href comme ceci :</br>

`<p><a href="mailto:votrenom@bidule.com">Envoyez-moi un e-mail !</a></p>`

Les liens permettent de changer de page et sont, par défaut, écrits en bleu et soulignés.
Pour insérer un lien, on utilise la balise `<a>` avec l'attribut href pour indiquer l'adresse de la page cible.</br> Exemple : `<a href="http://www.siteduzero.com">`.</br>
On peut faire un lien vers une autre page de son site simplement en écrivant le nom du fichier : `<a href="page2.html">`.</br>

Les liens permettent aussi d'amener vers d'autres endroits sur la même page.</br> Il faut créer une ancre avec l'attribut id pour « marquer » un endroit dans la page, puis faire un lien vers l'ancre comme ceci : `<a href="#ancre">`.</br>

###LES IMAGES###

Il existe plusieurs formats d'images adaptées au Web :</br>
`JPEG` : pour les photos ;</br>
`PNG` : pour toutes les autres illustrations ;</br>
`GIF` : similaire au `PNG`, plus limité en nombre de couleurs mais qui peut être animé.</br>
On insère une image avec la balise <img />.</br> Elle doit obligatoirement comporter au moins ces deux attributs : `src` (nom de l'image) et `alt` (courte description de l'image).</br>
Si une image illustre le texte (et n'est pas seulement décorative), il est conseillé de la placer au sein d'une balise `<figure>`.</br> La balise `<figcaption>` permet d'écrire la légende de l'image.</br>


###METTRE EN PLACE LE CSS###

CSS est un autre langage qui vient compléter le HTML. Son rôle est de mettre en forme votre page web.</br>
Il faut être vigilant sur la compatibilité des navigateurs avec certaines fonctionnalités récentes de CSS3.</br> Quand un navigateur ne connaît pas une instruction de mise en forme, il l'ignore simplement.</br>
On peut écrire le code CSS à plusieurs endroits différents, le plus conseillé étant de créer un fichier séparé portant l'extension .</br>css (exemple : style.css).
En CSS, on sélectionne quelles portions de la page HTML on veut modifier et on change leur présentation avec des propriétés CSS :</br>
`balise1
{
    propriete1: valeur1;
    propriete2: valeur2;
}`
Il existe de nombreuses façons de sélectionner la portion de la page que l'on veut mettre en forme. Par exemple, on peut viser :</br>
toutes les balises d'un même type, en écrivant simplement leur nom (h1 par exemple) ;</br>
certaines balises spécifiques, auxquelles on a donné des noms à l'aide des attributs `class` ou `id` `.nomclasse` ou `#nomid` ;</br>
uniquement les balises qui se trouvent à l'intérieur d'autres balises `h3` `em`.
etc.</br>

###FORMATAGE DU TEXTE##

On modifie la taille du texte avec la propriété CSS `font-size`. On peut indiquer la taille en pixels `16px`, en « `em` » `1.3em`, en pourcentage `110%`, etc.</br>
On change la police du texte avec `font-family`. Attention, seules quelques polices sont connues par tous les ordinateurs.</br> Vous pouvez cependant utiliser une police personnalisée avec la directive `@font-face` : cela forcera les navigateurs à télécharger la police de votre choix.</br>
De nombreuses propriétés de mise en forme du texte existent : `font-style` pour `l'italique`, `font-weight` pour la mise en gras, `text-decoration` pour le soulignement, etc.</br>
Le texte peut être aligné avec `text-align`.</br>
On peut faire en sorte qu'une image soit habillée (« entourée ») de texte avec `float`.</br>

###LA COULEUR ET LE FOND###

On change la couleur du texte avec la propriété color, la couleur de fond avec background-color.</br>
On peut indiquer une couleur en écrivant son nom en anglais (black, par exemple), sous forme hexadécimale `#FFC8D3` ou en notation RGB `rgb 250,25,118`.</br>
On peut ajouter une image de fond avec `background-image`. On peut choisir de fixer l'image de fond, de l'afficher en mosaïque ou non, et même de la positionner où on veut sur la page.</br>
On peut rendre une portion de la page transparente avec la propriété opacity ou avec la notation `RGBa` (identique à la notation RGB, avec une quatrième valeur indiquant le niveau de transparence).</br>

###LES BORDURES ET LES OMBRES###

On peut appliquer une bordure à un élément avec la propriété border. Il faut indiquer la largeur de la bordure, sa couleur et son type (trait continu, pointillés…).</br>
On peut arrondir les bordures avec `border-radius`.</br>
On peut ajouter une ombre aux blocs de texte avec `box-shadow`.</br> On doit indiquer le décalage vertical et horizontal de l'ombre, son niveau d'adoucissement et sa couleur.</br>
Le texte peut lui aussi avoir une ombre avec `text-shadow`.</br>

###CRÉATION D'APPARENCES DYNAMIQUES###

En résumé</br>

En CSS, on peut modifier l'apparence de certaines sections dynamiquement, après le chargement de la page, lorsque certains évènements se produisent. On utilise pour cela les pseudo-formats.</br>
Le pseudo-format `:hover` permet de changer l'apparence au survol (par exemple : `a:hover` pour modifier l'apparence des liens lorsque la souris pointe dessus).</br>
Le pseudo-format :active modifie l'apparence des liens au moment du clic, `visited` lorsqu'un lien a déjà été visité.</br>
Le pseudo-format :focus permet de modifier l'apparence d'un élément sélectionné.</br>




###STRUCTURER SA PAGE###


Plusieurs balises ont été introduites avec HTML5 pour délimiter les différentes zones qui constituent la page web :</br>
`<header>` : en-tête ;</br>
`<footer>` : pied de page ;</br>
`<nav>` : liens principaux de navigation ;</br>
`<section>` : section de page ;</br>
`<aside>` : informations complémentaires ;</br>
`<article>` : article indépendant.</br>
Ces balises peuvent être imbriquées les unes dans les autres. Ainsi, une section peut avoir son propre en-tête.</br>
Ces balises ne s'occupent pas de la mise en page. Elles servent seulement à indiquer à l'ordinateur le sens du texte qu'elles contiennent. On pourrait très bien placer l'en-tête en bas de la page si on le souhaite.</br>
Le code `JavaScript HTML5shiv` permet de faire en sorte que ces balises soient reconnues pour les versions d'Internet Explorer antérieures à IE9.</br>

###LE MODÈLE DES BOÎTES###

On distingue deux principaux types de balises en HTML :
Le type `block` `(<p>, <h1>…)` : ces balises créent un retour à la ligne et occupent par défaut toute la largeur disponible. Elles se suivent de haut en bas.</br>
Le type `inline` `(<a>, <strong>…)` : ces balises délimitent du texte au milieu d'une ligne. Elles se suivent de gauche à droite.</br>
On peut modifier la taille d'une balise de type block avec les propriétés CSS `width` -largeur et `height` hauteur.</br>
On peut définir des minima et maxima autorisés pour la largeur et la hauteur : `min-width`, `max-width`, `min-height`, `max-height`.</br>
Les éléments de la page disposent chacun de marges intérieures `padding` et extérieures `margin`.</br>
S'il y a trop de texte à l'intérieur d'un bloc de dimensions fixes, il y a un risque de débordement. Dans ce cas, il peut être judicieux de rajouter des barres de défilement avec la propriété `overflow` ou de forcer la césure avec `word-wrap`.</br>

###LE POSITIONNEMENT EN CSS###


La mise en page d'un site web s'effectue en CSS. Plusieurs techniques sont à notre disposition.</br>
Le positionnement flottant avec la propriété `float` est l'un des plus utilisés à l'heure actuelle. Il permet par exemple de placer un menu à gauche ou à droite de la page.</br> Néanmoins, cette propriété n'a pas été initialement conçue pour cela et il est préférable, si possible, d'éviter cette technique.</br>
Le positionnement`inline-block` consiste à affecter un type `inline-block` à nos éléments grâce à la propriété `display`.</br> Ils se comporteront comme des inlines (placement de gauche à droite) mais pourront être redimensionnés comme des blocs (avec width et height). Cette technique est à préférer au positionnement flottant.</br>
Le positionnement absolu permet de placer un élément où l'on souhaite sur la page, au pixel près.</br>
Le positionnement `fixed` est identique au positionnement absolu mais l'élément restera toujours visible même si on descend plus bas dans la page.</br>
Le positionnement relatif permet de décaler un bloc par rapport à sa position normale.</br>
Un élément A positionné en absolu à l'intérieur d'un autre élément B (lui-même positionné en absolu, fixe ou relatif) se positionnera par rapport à l'élément B, et non par rapport au coin en haut à gauche de la page.</br>

