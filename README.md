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

## nav

La balise `nav` permet de définir une zone contenant des éléments de navigation, typiquement un menu.

Cette balise a un sens pour les moteurs de recherche par exemple : quand un robot est en train d'analyser le code d'une page HTML, la balise `nav` lui permet de repérer plus facilement les endroits où il pourra naviguer dans le site.

Exemple :

```html
<nav>
  <!-- Contenu du menu -->
</nav>
```

>On peut avoir plusieurs balises `nav` dans un document HTML

## ul & ol

Il existe 2 types de listes en HTML : les listes ordonnées `ol` (ordered list) et les listes non ordonnées `ul` (unordered list).

Une balise de liste contient **forcément** des **éléments de liste**, ou encore **list items** : `li`.

```html
<!-- Liste non ordonnée -->
<ul>
  <li><!-- ... --></li>
  <li><!-- ... --></li>
  <li><!-- ... --></li>
</ul>

<!-- Liste ordonnée -->
<ol>
  <li><!-- ... --></li>
  <li><!-- ... --></li>
  <li><!-- ... --></li>
</ol>
```

>Par défaut, à l'affichage, une liste non ordonnée affichera chaque élément précédé d'un point noir, alors qu'une liste ordonnée affichera chaque élément précédé du chiffre représentant sa position dans la liste

Pour structurer notre menu, on peut inclure dans la balise `nav` une liste non ordonnée, `ul` (unordered list) :

```html
<nav>
  <ul>
    <li>
      <a href="url">Mon premier lien</a>
    </li>
    <li>
      <a href="url">Mon second lien</a>
    </li>
    <!-- ... -->
  </ul>
</nav>
```

## a

La balise `a` permet d'insérer un lien dans le corps de la page.

### Structure

On utilisera, dans un premier temps, 2 attributs dans la balise `a` :

- href : l'URL vers laquelle on se rendra si on clique sur le lien
- target : On utilisera cet attribut avec la valeur `_blank` si on souhaite ouvrir le lien dans un nouvel onglet (utile dans le cas de liens externes)

```html
<!-- ... -->

<!-- Ce lien s'ouvrira dans un nouvel onglet -->
<a href="https://www.google.com" target="_blank">
  Un lien externe vers Google
</a>

<!-- Ce lien relatif amènera sur une autre page du site, dans le même onglet -->
<a href="produits.html">
  Produits
</a>

<!-- ... -->
```

>Le contenu affiché à l'écran se trouve entre le tag d'ouverture et le tag de fermeture
