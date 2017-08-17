---
title: "r1d20 : les couleurs"
slug: "r1d20-couleurs"
subtitle: "un thème assorti aux volets de la maison"
date: "2017-08-12T20:29:32+02:00"
lastmod: 2017-08-16T10:24:34+02:00 
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


### Chantier à venir : construire une palette de couleurs

Recherche de couleurs complémentaires pour colorer un thème assorti aux volets de la maison. En me fondant sur une nomenclature simple de type RVB et en m'inspirant d'assortiments comme ce "sable, pierre, plage, océan" trouvé dans l'explorateur Adobe Color : 

![AdobeColors](/img/adobe-colors-andy-stone-beach-ocean-diver.png) 


### Expérience-utilisateur

(section ajoutée le 16 août)

Pour approfondir, lisez cet article de Zack Gehin (UX designer) : [Don’t let your color palette be an airball](https://medium.com/ruxers/dont-let-your-color-palette-be-an-airball-30d0f0c14f16). Zack délivre quelques bons trucs pratiques. Comme cette invitation faite aux auteurs à prendre en considération la lisibilité et l'expérience-utilisateur dans différents environnements. De ne pas oublier les personnes qui utilisent l'app à l'extérieur en pleine lumière... 

Voici ses préconisations résumées en quatre points : 

#### 1. Vérifiez les Contrastes 
S'assurer que la palette de couleurs soit conforme aux standards de contraste. Le [WCAG 2.0](https://www.w3.org/TR/WCAG/#visual-audio-contrast) est là pour aider les designers à créer les meilleures expériences possibles. Ce [validateur de contraste](http://leaverou.github.io/contrast-ratio/) de Lea Verou aide à vérifier facilement vos choix de couleurs et typographies. 

#### 2. Choisissez des nuances ou des teintes de la même famille de couleurs

1. Identifiez votre couleur primaire. Peut-être que c'est du bleu comme vos futurs volets
2. Prenez cette couleur et générez ses nuances et la palette de teintures. [Colllor](http://colllor.com/), le générateur de palettes vous facilitera la tâche.
3. Une fois généré, faites une capture d'écran, identifiez une tonalité pour générer vos couleurs sombres. Créez de nouvelles nuances en fonction de cette couleur.
4. Maintenant, dans Sketch, déposez vos captures d'écran et choisissez des couleurs à partir du même emplacement à chaque échelle.

**Vous avez maintenant votre terrain de jeu**.

![Patience... Essais et erreurs pour une palette répondant à la spécification WCAG 2.0](/img/couleur/palette-couleurs.png)


#### Testez votre palette dans plusieurs environnemenets

L'une des étapes les plus importantes : identifier les environnements dans lesquelles les personnes utilisent votre app. Suivre le processus de design environnemental vous aidera à comprendre les différents environnements nécessaires. Placez votre terminal dehors à la lumière du jour, dans une salle sombre, ... et testez ! 

**Si quelque chose ne va pas, itérez !**


#### Regardez vos couleurs sur différents écrans 

Bien que bon nombre d'entre nous aient la chance de travailler sur les meilleures technologies, la plupart du monde ne l'est pas. Il est facile de s'habituer aux retina et/ou aux écrans 5k. Prenons du recul, sortez un portable Windows et un moniteur de faible qualité ; vous pourriez être surpris par ce que vous voyez. Un bon moyen d'identifier les machines et moniteurs à tester est d'extraire les données de Google Analytics ou de vos outils de statistiques.













 