---
title: "R1D4: formats de date dans GoHugo"
date: 2017-07-27
tags: [100daysofcode, log]
---

Premier post sur ce nouveau site dédié à compléter mon [log 100daysofcode](https://github.com/ChristopheDucamp/100-days-of-code-xtof). Bien installé dans les massifs à proximité de [Sank Pölten](https://fr.wikipedia.org/wiki/Sankt_Pölten). Temps pluvieux, les photos suivront demain... <!--more--> Excité de poser un [log 100daysofcode](https://github.com/ChristopheDucamp/100-days-of-code) sur une nouvelle motorisation GoHugo. ([thème multilingue "beautiful hugo"](https://github.com/halogenica/beautifulhugo).)

## Intention 

Améliorer ce site pour restituer des formats de date avec un  rendu d'affichage en français, "plus humain" et correct sémantiquement (ajouter la balise `time`).

- `mardi 1<sup>er</sup> août`
- `Donnerstag, 27 Juli` pour les amis autrichiens de [vienna.html](https://github.com/viennahtml) quand la mise en page des dates fonctionnera 

### Statut : travaux en cours 

**Objectif** : Personnaliser les dates dans les layouts avant l'ajout d'autres partiels dédié à quelques [briques de construction indieweb](https://indieweb.org/Category:building-blocks)

## Production du jour 

- Un repo github [`100daysofcode-site`](https://github.com/ChristopheDucamp/100-days-of-code-site) 

## Code et Ressources pour personnaliser la Date

### Code 

#### un fichier data `mois.yaml` 

(placé dans `data/mois.yaml`)

```yaml
1: "janvier"
2: "février"
3: "mars"
4: "avril"
5: "mai"
6: "juin"
7: "juillet"
8: "août"
9: "septembre"
10: "octobre"
11: "novembre"
12: "décembre"
```

#### un partiel pour imaginer un bouton de modification 

ala wiki, l'idée serait d'ajouter un bouton en bas de chaque post libellé "modifier la page" pointant sur le fichier github lié 

```golang
<!-- partiel de date publication et mise a jour au format fr a raffiner. ex : <nomdujour> 1er -->

dernière mise à jour le : 
<time class="dt-updated" datetime="{{ .Lastmod.Format "2006-01-02T15:04:05Z07:00" | safeHTML }}">{{ .Lastmod.Day }} {{ index $.Site.Data.mois (printf "%d" .Lastmod.Month) }} {{ .Lastmod.Year }}</time> <br> 

        {{ partial "page-edit.html" . }}
        
```

#### un partiel date de publication 

- à placer dans les posts et la page de liste des posts (dossier `layouts/default)


```golang
<time class="post-date dt-published" datetime="{{ .PublishDate.Format "2006-01-02T15:04:05Z07:00" | safeHTML }}">{{ .PublishDate.Day }} {{ index $.Site.Data.mois (printf "%d" .PublishDate.Month) }} {{ .PublishDate.Year }}</time>
```


### Ressources à étudier

- [GoHugo : multilingual mode / customize dates](https://gohugo.io/content-management/multilingual/#customize-dates)
- [Formatting a date with suffix (2nd)](https://discourse.gohugo.io/t/formatting-a-date-with-suffix-2nd/5701) - forum de discussion Hugo
- [Francisation de la date](https://github.com/nicolinuxfr/voiretmanger-hugo/commit/5ecc162a0e89d803997fff5e9ef0a2507c0ff6d0) - (repo voiretmanger- hugo)
- [Parsing dates in templates](https://discourse.gohugo.io/t/parsing-dates-in-templates/603/12)
- [Slack jamstatic](https://jamstatic-fr.slack.com/archives/C5MTQPL4E/p1500985424553770)
> tu peux découper ton {{.Date}} en {{.Day}} {{.Month}} et {{.Year}}
> ici un exemple de code où je récupère un timestamp PHP et je le convertis en date humaine :

```php
Publié le {{$time := time (div (int .Params.dateAdd) 1000)}}{{ $monthindex := index $.Site.Data.mois (printf "%d" $time.Month) }} {{$time.Day}} {{$monthindex}} {{$time.Year}}
```

