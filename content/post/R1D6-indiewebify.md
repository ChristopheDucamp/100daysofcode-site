---
title: "R1D6 : "
date: 2017-07-29
date: 2017-07-29 
tags: [indieweb]
bigimg: [{src: "/img/bureau-autriche-campagne.jpg", desc: "2ème bureau"}]
---

## Création et Mise en Forme du Bouton "Améliorer cette page"

- Création d'un partiel '/partials/page-edit.html` avec un bloc de [composants CSS bootstrap](https://v4-alpha.getbootstrap.com/components/buttons/)

```
<div class="btn btn-primary btn-lg btn-block">
Page mise à jour le 
<time class="dt-updated" datetime="{{ .Lastmod.Format "2006-01-02T15:04:05Z07:00" | safeHTML }}">
{{ .Lastmod.Day }} {{ index $.Site.Data.mois (printf "%d" .Lastmod.Month) }} {{ .Lastmod.Year }}
</time> 
<a class="btn btn-primary btn-success white hover-bg-green link" role="button" 
href="{{.Site.Params.ghrepo}}edit/master/content/{{.File.Path}}">
Améliorez cette page</a>
</div>
```

## indiewebification 
### article (variable à trouver)

- ajouter un auteur (variable dans les métadonnées)
<a rel="author" class="p-author h-card" href="…">Your Name</a>
- ajouter url <a class="u-url" href="…">…</a>



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

