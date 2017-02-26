# ScrollShow---Easy-Scroll-Animation
Gérer les apparitions au scroll très simplement

<h2> Installation </h2>

`<script src="https://code.jquery.com/jquery-3.1.1.min.js"></script> <!-- Librairie Jquery necessaire -->
 <script src="js/showScroll.js"></script> <!-- Fichier necessaire aux animations -->`
 

<h2> Syntaxe globale </h2>

<h4>Apparition d'un élément seul</h4>

`<div class="showScroll [classe de l animation] [classes optionnelles]"></div>`

<h2> Syntaxe particulière - Objets liés </h2>

<h4>Apparition de plusieurs éléments pour l'atteinte du scroll d'un élément parent</h4>

`<div class="showScrollContainer">`
 <br/>
    `<div class="showScrollElement [classe de l animation] [classes optionnelles] [delay] [ordre]"></div>`
   <br/>
    `<div class="showScrollElement [classe de l animation] [classes optionnelles] [delay] [ordre]"></div>`
   <br/>
`</div>`

- delay : si un délai est voulu avant l'apparition d'un élément (et donc entre chaque élément)
    - S'écrit : "delay-" + [valeur de type numérique (ms)] 

- ordre : si un ordre particulier d'apparition est voulu (qui n'est pas l'ordre des objets en HTML)
    - S'écrit : "show-" + [position (commence à 1)]
    - Particularité :
       - ne pas mettre 2 éléments à la même position. S'ils soivent apparaitre en même temps, assignez-leur des positions    consécutives et un délai de 0
       - ne pas sauter de position (ex. passer de show-1 à show-3 sans qu'aucun élément show-2 existe)

 
 
 <h2> Paramètres par défaut </h2>
 
<h3> delay </h3>

- <strong>Définition :</strong> Délai avant la suppression d'un élément en ms
- <strong>Valeurs possibles :</strong> valeurs numériques uniquement 

<h3> hide </h3>

- <strong>Définition :</strong> Où est caché un élément avant d'apparaître
- <strong>valeurs possibles :</strong> 
   - "window" : sort de l'écran
   - "self" : est décalé de lui-même X fois
   - Valeur numérique en px (exemple "200")

<h3> times </h3>

- <strong>Définition :</strong> Si hide="self", nombre de fois que l'élément sera décalé de lui-même
- <strong>Valeurs possibles :</strong> valeurs numériques uniquement 

<h3> scaleStart </h3>

- <strong>Définition :</strong> Taille initiale d'un élément avant son apparition
- <strong>Valeurs possibles :</strong> valeurs numériques uniquement 

<h3> scaleEnd </h3>

- <strong>Définition :</strong> Taille finale d'un élément après son apparition
- <strong>Valeurs possibles :</strong> valeurs numériques uniquement 

<h3> fadeStart </h3>

- <strong>Définition :</strong> Opacité initiale d'un élément avant son apparition
- <strong>Valeurs possibles :</strong> Valeurs numériques entre 0 et 1

<h3> fadeEnd </h3>

- <strong>Définition :</strong> Opacité finale d'un élément avant son apparition
- <strong>Valeurs possibles :</strong> Valeurs numériques entre 0 et 1

<h3> tour </h3>

- <strong>Définition :</strong> Nombre de tours que fera un élément en apparaissant en mode "rotation"
- <strong>Valeurs possibles :</strong> Valeurs numériques
- <strong>Sens :</strong>
    - Nombre positif : rotation antihoraire
    - Nombre négatif : rotation horaire

<h3> anchor </h3>

- <strong>Définition :</strong> Point d'ancrage d'un élément = où va-t-on le détecter
- <strong>Valeurs possibles :</strong> 
   - "top" : Haut de l'élément
   - "center" : Centre de l'élément
   - "bottom" : Bas de l'élément
   
<h3> limit </h3>

- <strong>Définition :</strong> Le point où l'animation de l'élément va se déclencher
- <strong>Valeurs possibles :</strong> 
   - nombre : nombre de pixels à partir du haut de l'écran (ex. "200")
   - "centerWindow" : Centre de la fenêtre
   - "bottomWindow" : Bas de la fenêtre
   
<h3> les transitions </h3>
- <strong> transitionOpacity :<strong> : durée de transition concernant l'opacité
- <strong> transitionMoveFromLeft :<strong> : durée de transition concernant les éléments arrivant par la gauche
- <strong> transitionMoveFromRight :<strong> : durée de transition concernant les éléments arrivant par la droite
- <strong> transitionTransform :<strong> : durée de transition concernant la rotation et la taille
   
   <h2> Comment les utiliser ? </h2>
   
   - 1 classe obligatoire
   - Des classes optionnelles construites de la sorte :
      - [paramètre] + "-" + [valeur]
   
   <h3> Je veux que mon élément apparaisse en fondu </h3>
   
   - classe obligatoire : "fade"
   - classes optionnelles : 
      - "fadeStart-"+[valeur]
      - "fadeEnd-"+[valeur]
      
   <h3> Je veux que mon élément apparaisse en zoom/dézoom </h3>
   
   - classe obligatoire : "scale"
   - classes optionnelles : 
      - "scaleStart-"+[valeur]
      - "scaleEnd-"+[valeur]
      
  <h3> Je veux que mon élément apparaisse de droite à gauche </h3>
   
   - classe obligatoire : "rightToLeft"
   - classes optionnelles : 
      - "hide-"+[valeur]
      - "times"+[valeur] (si "hide-self")
      
   <h3> Je veux que mon élément apparaisse de gauche à droite </h3>
   
   - classe obligatoire : "leftToRight"
   - classes optionnelles : 
      - "hide-"+[valeur]
      - "times"+[valeur] (si "hide-self")
      
   <h3> Je veux que mon élément apparaisse en tournant </h3>
   
   - classe obligatoire : "rotation"
   - classes optionnelles : 
      - "tour-"+[valeur]

