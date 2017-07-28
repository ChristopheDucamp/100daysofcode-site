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


## todo 

### [indiewebification](https://indiewebify.me/validate-rel-me/?url=https%3A%2F%2F100daysofcode.christopheducamp.com)

Ajouter les [briques de construction indieweb](https://adactio.com/journal/7698) essentielles

- pied de page à travailler 
	- personnaliser variable `site` pour `author` avec linkback
	- [h-card](http://microformats.org/wiki/h-card) et rel="me" sur les icônes sociales

### Archétypes 

- à personnaliser (ajouter tags, bigimg...)


### Iconographie 

- Ajouté un répertoire local `static/img` pour ajouter des images personnelles
- Shortcode `gallery` à tester (modèle [Photoswipe](/post/echantillon-photoswipe-gallery))

{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-thumb" link="/img/hexagon.jpg" >}}
  {{< figure thumb="-thumb" link="/img/sphere.jpg" caption="Sphere" >}}
  {{< figure thumb="-thumb" link="/img/triangle.jpg" caption="Triangle" alt="Ceci est long commentaire concernant un triangle" >}}
{{< /gallery >}}
