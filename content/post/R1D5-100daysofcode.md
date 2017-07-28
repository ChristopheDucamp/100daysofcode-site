---
title: "R1D5 : FuckingGoDateFormat, https et un lien `Améliorez la Page`"
date: 2017-07-28T11:40:36+02:00
lastmod: 2017-07-28T19:40
draft: false
bigimg: [{src: "/img/path.jpg", desc: "Sur la Route"}]
tags: [100daysofcode, https, dates]
---

<!--more-->



- déploiement netlify : ajout certificat https 
- poursuite du chantier pour mettre toutes les [dates en français](R1D4-100daysofcode). [FuckingGoDateFormat](http://fuckinggodateformat.com/)
	- ajouté une date de modification en pied de page
- ajout d'un lien "améliorez cette page" vers repo github.
- complété l'[archétype](https://gohugo.io/content-management/archetypes/#readout) `default.md` avec les types de contenu `lastmod`, `tags`, `bigimg`.
- Réglé le fichier de configuration pour ajouter la date dans le schéma URL suivant (faute d'équivalent du `%j` jour de l'année qui n'existe pas nativement en Go.)

```toml
[permalinks]
  post = "/:year/:month/:day/:title/"
```

<!--
## todo 



### [indiewebification](https://indiewebify.me/validate-rel-me/?url=https%3A%2F%2F100daysofcode.christopheducamp.com)

#### briques basiques

Ajouter les [briques de construction indieweb](https://adactio.com/journal/7698) essentielles

- pied de page à travailler 
	- personnaliser variable `site` pour `author` avec linkback
	- [h-card](http://microformats.org/wiki/h-card) représentative sur URL avec photo 
	- rel="me" sur les icônes sociales
- ajouter `h-entry` aux articles

```html
<article class="h-entry">
  <div class="e-content p-name">Hello world! This is my first indieweb post.</div>

  <a class="u-url" href="https://exemple.com/my-first-post">
    Publié le <time class="dt-published">2017-07-28 11:10:22+0000</time>
  </a>
</article>
```

#### webmentions

ressources à trouver

- <https://github.com/ChristopherA/LifeWithAlacrityBlog/tree/master/blog/themes/indie-tufte>
- <http://www.petersell.com/2017/indiewebify-my-static-hugo-website>


### Iconographie 

- Ajouté un répertoire local `static/img` pour ajouter des images personnelles
- Shortcode `gallery` à tester (modèle [Photoswipe](/post/echantillon-photoswipe-gallery))

{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-thumb" link="/img/hexagon.jpg" >}}
  {{< figure thumb="-thumb" link="/img/sphere.jpg" caption="Sphere" >}}
  {{< figure thumb="-thumb" link="/img/triangle.jpg" caption="Triangle" alt="Ceci est long commentaire concernant un triangle" >}}
{{< /gallery >}}

-->