---
title: Échantillon "Photoswipe Gallery"
subtitle: Produire une Galerie
date: 2017-03-20
tags: ["exemple", "photoswipe"]
---

Le thème Beautiful Hugo ajoute quelques shortcodes personnalisés créés par [Li-Wen Yip](https://www.liwen.id.au/heg/) et [Gert-Jan van den Berg](https://github.com/GjjvdBurg/HugoPhotoSwipe) pour produire des galleries avec [PhotoSwipe](http://photoswipe.com) . 

{{< gallery caption-effect="fade" >}}
  {{< figure thumb="-thumb" link="/img/hexagon.jpg" >}}
  {{< figure thumb="-thumb" link="/img/sphere.jpg" caption="Sphere" >}}
  {{< figure thumb="-thumb" link="/img/triangle.jpg" caption="Triangle" alt="This is a long comment about a triangle" >}}
{{< /gallery >}}

<!--more-->
## Exemple
La galerie au-dessus a été créée en utilisant les shortcodes suivants: 
```
{{</* gallery caption-effect="fade" */>}}
  {{</* figure thumb="-thumb" link="/img/hexagon.jpg" */>}}
  {{</* figure thumb="-thumb" link="/img/sphere.jpg" caption="Sphere" */>}}
  {{</* figure thumb="-thumb" link="/img/triangle.jpg" caption="Triangle" alt="This is a long comment about a triangle" */>}}
{{</* /gallery */>}}
```

## Usage
Pour les détails complets d'installation, regardez la page [GitHub hugo-easy-gallery GitHub](https://github.com/liwenyip/hugo-easy-gallery/). Les usages basiques au-dessus sont : 

- Créez une galerie avec des balises d'ouverture et de fermeture `{{</* gallery */>}}` and `{{</* /gallery */>}}`
- `{{</* figure src="image.jpg" */>}}` utilisera  `image.jpg` pour la vignette et la lightbox
- `{{</* figure src="thumb.jpg" link="image.jpg" */>}}` utilisera `thumb.jpg` pour la vignette et  `image.jpg` pour la lightbox
- `{{</* figure thumb="-small" link="image.jpg" */>}}` utilisera `image-small.jpg` pour la vignette et `image.jpg` pour la lightbox
- Tous les [fonctionnalités/paramètres](https://gohugo.io/extras/shortcodes) du shortcode intégré de Hugo `figure` fonctionneront normalement, c'est-à-dire `src`, `link`, `title`, `caption`, `class`, `attr` (attribution), `attrlink`, `alt`
- `{{</* gallery caption-effect="fade" */>}}` Disparaîtra dans les légendes pour toutes les figures de cette galerie au lieu du comportement de glissement par défaut

will fade in captions for all figures in this gallery instead of the default slide-up behavior
- Many gallery styles for captions and hover effects exist; view the [hugo-easy-gallery GitHub](https://github.com/liwenyip/hugo-easy-gallery/) for all options
- Notez que ce thème chargera par défaut le thème photoswipe gallery et les scripts, nul besoin de charger photoswipe sur vos pages individuelles.