# Introduction

- HTML = HyperText Markup Language
- CSS = Cascading StyleSheet
- JS = JavaScript

Dans un modèle client/serveur sur le web, le client est le navigateur. Dans ce module, nous allons faire du développement côté client (statique, sans serveur).

## Balises HTML

Le HTML est composé de **balises**.

Pour écrire une balise, on utilise la syntaxe suivante :

```html
<balise>...</balise>
```

Il existe également des balises **auto fermantes**. Elles n'ont pas de tag de fermeture et le tag d'ouverture se ferme avec un `/` avant le chevron :

```html
<!-- Exemple avec br pour un retour à la ligne -->
<br />
```

## Retours à la ligne

>Les retours à la ligne écrits dans le code n'ont aucun effet sur l'affichage dans le navigateur. Utilisez la balise `<br />` pour effectuer un retour à la ligne. Nous verrons également plus tard comment styliser des éléments pour paramétrer la marge supérieure, inférieure, l'espacement, etc...

## Attributs de balises HTML

Une balise ouvrante peut avoir un ou plusieurs attributs. On renseignera le nom de l’attribut et sa valeur entre guillemets :

```html
<!-- Ici on définit un attribut "lang" qui a pour valeur "fr" -->
<html lang="fr">...</html>
```

## Les balises `head` et `body`

La balise `head` définit les métadonnées sur le document HTML. On va définir un titre, des imports de CSS, de JS, de polices de caractères (fonts), le jeu de caractères utilisé dans la page, etc…

>head est obligatoire.

La balise `body` contient le corps de la page : ce qui est affiché à l’écran, dans le navigateur. C’est le contenu de notre page : titre(s), menu, sections, etc…

>body est obligatoire.
---
>Les balises `head` et `body` sont les enfants directs de la balise racine `html`

## Images

La balise `img` est une balise auto fermante.

L'attribut `src` de `img` permet de préciser le chemin vers l'image à afficher.

Il y a 2 types de chemin possibles :

### Chemin absolu

C’est le chemin **COMPLET** d’accès à l’image (URL complète, depuis « https » jusqu’à l’extension (".png" par exemple))

### Chemin relatif

C’est un chemin relatif au document HTML courant. Le navigateur va chercher le fichier renseigné à partir du dossier dans lequel se trouve le document HTML
