---
title: "R1D7 Indiemark Niveau 1"
date: 2017-07-30T06:55:03+02:00
draft: false
tags: [indieweb]
bigimg: [{src: "/img/path.jpg", desc: "Sur la Route"}]
---

## IndieMark Niveau 1

- [Référence](https://indieweb.org/IndieMark#Level_1) 
- inspiré par le thème Hugo "[indie-tufte](https://github.com/ChristopherA/LifeWithAlacrityBlog/tree/master/blog/themes/indie-tufte)" de Kevin Marks

### partial h-card 

Une h-card représentative est appelée dans le footer par le partiel suivant :

```
<span class="h-card">
<img class="u-photo" src="{{ .Site.Author.authorphoto }}" /> <a rel="me" href="{{ .Site.Author.site }}" >{{ .Site.Author.name }}</a>
</span>
```

Le validateur suggère l'ajout d'un e-mail et d'une note/bio

```
<a rel="me" class="u-email">…</a>
<p class="p-note">…</p>
```



### Posts 

- Modifié le fichier de configuration pour rajouter des variables de site `Author`.
- ajouté un partiel `auteur.html` 

```
<a rel="author" class="p-author h-card" href="{{ .Site.Author.authorurl }}">{{ .Site.Author.name }}</a>

```

- ajouter url ```<a class="u-url" href="…">…</a>```



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

