# ScrollShow---Easy-Scroll-Animation
Gérer les apparitions au scroll très simplement

<h2> Installation </h2>

`<script src="https://code.jquery.com/jquery-3.1.1.min.js"></script> <!-- Librairie Jquery necessaire -->
 <script src="js/showScroll.js"></script> <!-- Fichier necessaire aux animations -->`
 
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
