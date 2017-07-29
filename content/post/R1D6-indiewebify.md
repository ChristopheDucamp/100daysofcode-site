---
title: "R1D6 : Premiers pas pour indiewebifier Hugo"
date: 2017-07-29
tags: [indieweb]
bigimg: [{src: "/img/pente-ecole-autriche.jpg", desc: "2ème bureau"}]
---

Installé un 2ème bureau pour travailler au calme au pied d'une "future pente-école" pour le parapente. 
La maison est désormais réveillée, les travaux matinaux s'arrêteront là. 2 heures pour créer un bouton "Améliorez cette page", aménager un un dossier pour déposer mes futures photos d'excursions. Et amorcer les étapes d'indiewebification.<!--more-->

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
## Iconographie 

- Ajouté un répertoire local `static/img` afin d'ajouter des images personnelles et reprendre un vieux défi de poster une photo par jour qui pourrait se placer dans la bannière.
- Galerie dans les posts : test du shortcode `gallery` (modèle [Photoswipe](/post/echantillon-photoswipe-gallery))

{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-thumb" link="/img/pente-ecole-autriche.jpg" caption="vue de mon bureau">}}
  {{< figure link="/img/bureau-autriche-campagne.jpg" caption="2ème bureau" alt="Mon 2ème bureau dans le jardin" >}}
  {{< figure thumb="-thumb" link="/img/sphere.jpg" caption="Sphere" >}}

  
{{< /gallery >}}
## IndieMark Niveau 1

Le web indépenant classique + IndieAuth

> IndieMark Level 1 has the general theme of owning your own domain, for sign-in, and publishing posts

- Référence <https://indieweb.org/IndieMark#Level_1>
- Validateur : <https://indiewebify.me/>

### connexion web (web sign-in)

- modifié (provisoirement, pour 100 jours...) mon profil twitter avec l'url de ce site afin de faire fonctionner un "linkback".

![indiewebify linkback](https://monosnap.com/file/OO15UsKvvLM1bapRijTPClLENBwdXt.png)
### todo du soir  
#### validation h-card 

Trop de h-cards selon le validateur indiewebify :  

![indiewebify.me](https://monosnap.com/file/caUAs9rggeCEReojYWzG9WLh8j4EnH.png)

- Modifié le fichier de configuration pour rajouter des variables de site `Author`.
- Installé dans un partiel `hcard.html` une h-card représentative inspirée du [modèle de Kevin Marks](https://github.com/ChristopherA/LifeWithAlacrityBlog/blob/master/blog/themes/indie-tufte/layouts/partials/hcard.html)

```
<div class="h-card">
<img class="u-photo" src="{{ .Site.Author.authorphoto }}" />
<h1><a href="{{ .Site.Author.authorurl }}" >{{ .Site.Author.name }}</a><h1>
</div>
```

##### email  

```html
<a rel="me" class="u-email" mailto:"{{ .Site.Author.authorurl }}">{{ .Site.Author.email }}</a>
```

##### ajouter une note / minibio
```html
<p class="p-note">{{ .Site.Author.summary }}</p>
```

#### article (variables à raffiner)

- ajouter un auteur 

```
<a rel="author" class="p-author h-card" href="{{ .Site.Author.authorurl }}">{{ .Site.Author.name }}</a>
```

- ajouter url ```<a class="u-url" href="…">…</a>```

<!--

### briques basiques (Niveau 1 et 2)

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

### avancé 
#### webmentions

ressources à compléter : 

- [So long Disqus, hello Webmention](https://nicolas-hoizey.com/2017/07/so-long-disqus-hello-webmentions.html) Nicolas Hoizey - 2017-07-27 (plugin Jekyll)
-  [indie-tufte](https://github.com/ChristopherA/LifeWithAlacrityBlog/tree/master/blog/themes/indie-tufte) - thème hugo de Kevin Marks
- [indiewebify my static hugo web site](http://www.petersell.com/2017/indiewebify-my-static-hugo-website)


-->
