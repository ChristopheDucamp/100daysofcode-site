---
title: "R1D7 Indiemark Niveau 1-3 - posts"
date: 2017-07-30T06:55:03+02:00
draft: false
tags: [indieweb]
bigimg: [{src: "/img/arc-en-ciel-autriche.jpg", desc: "arc-en-ciel"}]
---

## Chantier IndieMark Niveau 1

- [Référence indieweb](https://indieweb.org/IndieMark#Level_1) 
- Inspiration thème Hugo "[indie-tufte](https://github.com/ChristopherA/LifeWithAlacrityBlog/tree/master/blog/themes/indie-tufte)" de Kevin Marks

Statut : chantier indieweb. Où placer le `h-entry` <https://indiewebify.me/validate-h-entry/> dans le thème "beautiful-hugo" ?

<!--more-->

### Création d'un partiel `h-card.html` 

Une h-card représentative est désormais appelée dans le footer par le partiel suivant 

```
<span class="h-card">
<img class="u-photo"   
src="{{ .Site.Author.authorphoto }}" />   
<a rel="me" href="{{ .Site.Author.site }}"  
>{{ .Site.Author.name }}</a>
</span>
```

Le validateur suggère l'ajout d'un e-mail et d'une note/bio

```
<a rel="me" class="u-email">…</a>
<p class="p-note">…</p>
```


### Posts 
#### Instructions

Vos "h-entries" devraient avoir, au minimum, les propriétés suivantes :

  * `e-content` — le contenu principal du post
  * `p-name` — si votre post a un nom, utilisez ce nom de classe. Autrement, (si par exemple le post est une [note](https://indieweb.org/note)), laissez tomber ou appliquez le même élément comme `e-`.
  * `dt-published` — le "datetime" auquel le post a été publié, en format ISO8601, avec un "timezone"
  * `u-url` — l'URL canonique du post, tout spécialement importante sur les pages répertoriant plusieurs posts.

C'est une convention commune pour le datetime publié d'être un lien vers le post en lui-même, mais il peut être séparé.

Il devrait y avoir aussi un moyen de découvrir l'auteur du post  — soit un lien vers la page d'accueil (qui devrait avoir votre h-card) à partir de n'importe où sur la page avec `rel=author`, ou facultativement embarquer un `p-author h-card` dans le `h-entry`.

Voir la [doc h-entry](https://microformats.org/wiki/h-entry) pour une liste complète.

#### Travaux en cours sur variables

- Modifié le fichier de configuration pour rajouter des variables de site `Author`.
- ajouté un partiel `auteur.html` dans `post-meta.html` (style à travailler)

```
<a rel="author" class="p-author h-card" 
href="{{ .Site.Author.authorurl }}"> 
{{ .Site.Author.name }}</a>
```

#### À travailler

- [entry.html](https://github.com/ChristopherA/LifeWithAlacrityBlog/blob/master/blog/themes/indie-tufte/layouts/_default/entry.html) ... 
- Ajouter une url de permalien (variable `.Permalink) dans le titre du contenu ```<a class="u-url" href="…">…</a>``` 

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
- [indiewebify my static hugo web site](http://www.petersell.com/2017/indiewebify-my-static-hugo-website)

-->

