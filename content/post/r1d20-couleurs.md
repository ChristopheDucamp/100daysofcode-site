---
title: "r1d20 en couleurs"
slug: "r1d20-couleurs"
subtitle: "un thème assorti aux volets de la maison ?"
date: "2017-08-12T20:29:32+02:00"
lastmod: 2017-08-13T13:18:30+02:00 
draft: false
tags: [100daysofcode, colors, graphisme]
bigimg: [{src: "/img/arc-en-ciel-autriche.jpg", desc: "arc en ciel - Autriche"}, {src: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/Optical-dispersion.png/220px-Optical-dispersion.png", desc: "Pink Floyd - Prisme"}]
---

20ème journée consacrée à la [section Graphisme](https://github.com/GoesToEleven/html-css-bootcamp) sur les bases de l'excellent bootcamp html/css de Todd McLeod. Une grosse section qui couvre les couleurs, les images et l'extraction d'icônes en SVGs. <!--more-->

## Démarrage par la Couleur

Dans la vraie vie, les graphistes, décorateurs, professionnels de la peinture, du tissu, de l'imprimerie... travaillent tous avec des codes de couleurs qui peuvent se convertir plus ou moins aisément. 

![Le Capsure de Pantone](/img/pantone-capsure-bluetooth.png)

> La propriété **`color`** permet de paramétrer la couleur de premier plan d'un élément texte et de ses éventuelles [décorations](https://developer.mozilla.org/fr/docs/Web/CSS/text-decoration). -- source [MDN: color](https://developer.mozilla.org/fr/docs/Web/CSS/color)

La propriété CSS **`<color>`** permet de représenter précisément des couleurs dans [l'espace de couleurs sRGB](https://fr.wikipedia.org/wiki/SRGB). 

Une couleur peut être décrite de trois façons :

  1. grâce à un mot-clé 
  2. en utilisant [le système de coordonnées cubiques RGB](https://fr.wikipedia.org/wiki/Couleur_du_Web#Triplet_hexad.C3.A9cimal) (grâce à la notation #-hexadecimal ou aux notations fonctionnelles `rgb()` et `rgba()`)
  3. ou en utilisant [le système de coordonnées cylindriques HSL](https://fr.wikipedia.org/wiki/Teinte_saturation_lumi%C3%A8re) (grâce aux notations fonctionnelles  `hsl()` et `hsla()`)

Bien que les valeurs de couleur CSS soient définies avec précision, elles peuvent apparaître différemment selon les terminaux, la plupart des écrans de terminaux n'étant pas calibrés. Le rendu des couleurs peut donc beaucoup varier. 

### Ressources utiles

- [Valeurs communes de propriété color en CSS](http://learn.shayhowe.com/html-css/getting-to-know-css/#css-property-values) - Shay Howe
- Roue [Adobe Color CC](https://color.adobe.com/fr/create/color-wheel/)
- [convertisseur décimal en hexadécimal (base 16)](http://www.binaryhexconverter.com/decimal-to-hex-converter)


### Usage à venir 

Recherche en cours de couleurs complémentaires pour colorer un thème assorti aux volets de la maison. En me fondant sur une nomenclature simple de type RVB et en m'inspirant d'assortiments comme ce "sable, pierre, plage, océan" trouvé dans l'explorateur Adobe Color : 

![AdobeColors](/img/adobe-colors-andy-stone-beach-ocean-diver.png) 