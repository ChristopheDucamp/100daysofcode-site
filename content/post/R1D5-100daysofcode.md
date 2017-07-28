---
title: "R1D5 100daysofcode : ajout https, h-card"
date: 2017-07-28T11:40:36+02:00
draft: false
bigimg: [{src: "/img/path.jpg", desc: "Sur la Route"}]
tags: [100daysofcode, hcard, https, indieweb]
---

## Production du jour
<!--more-->

- ajouté certificat https 
- bataillé pour poser des [dates en français](R1D4-100daysofcode) (chantier en cours)
- pied de page : 
	- ajout variable `site` pour `author`, 
	- h-card et rel="me" sur les icônes sociales

## todo 

### Archétypes 

- à personnaliser (ajouter tags, bigimg...)


### Iconographie 

- Ajouté un répertoire local `static/img` pour ajouter des images personnelles
- Shortcode {{< gallery >}} à tester ce soir selon modèle :

```
{{< gallery >}}
  {{< figure src="image1.jpg" >}}
  {{< figure src="image2.jpg" >}}
  {{< figure src="image3.jpg" >}}
{{< /gallery >}}
```

avec légende d'images et effet "fade" 
 
```yaml
{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-thumb" link="/img/hexagon.jpg" >}}
  {{< figure thumb="-thumb" link="/img/sphere.jpg" caption="Sphere" >}}
  {{< figure thumb="-thumb" link="/img/triangle.jpg" caption="Triangle" alt="Ceci est long commentaire concernant un triangle" >}}
{{< /gallery >}}
```
