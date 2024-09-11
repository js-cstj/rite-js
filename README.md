# Le "rite de passage"

**But du rite de passage** : Démontrer sa capacité à suivre des instructions simples et à transposer ces directives dans divers contextes.

Pour satisfaire au rite de passage, **tous** les élèves devront être capables de recomposer n'importe quelle arborescence de balises HTML donnée par le professeur.

---

## Les vidéos

Suivez le [tutoriel](https://www.youtube.com/watch?v=1gCWSWQ5ESE&list=PLR5YZQKvy9U1k3hdBGOQo24dw6ZokK-oK) incluant 5 vidéos

[![Vidéo Youtube](https://img.youtube.com/vi/1gCWSWQ5ESE/0.jpg "Playlist Rite de passage")](https://www.youtube.com/watch?v=1gCWSWQ5ESE&list=PLR5YZQKvy9U1k3hdBGOQo24dw6ZokK-oK)

---

## Étape 1 - La balise

Ajouter des balises simples une à la suite de l'autre.

### Les nouveaux mots-clés de l'étape 1

**En résumé** : `getElementById`, `createElement`, `appendChild` et `innerHTML`

```javascript
//Récupérer l'élément HTML dont l'attribut id a la même valeur que un_id.
element = document.getElementById(un_id); 

// Créer un élément HTML (balise) vide dont le nom correspond à la valeur de une_balise
element = document.createElement(une_balise); 

// Ajouter un elementEnfant à la fin du contenu d'un elementParent
elementParent.appendChild(elementEnfant); 

// Définit le contenu HTML d'une balise
element.innerHTML = "Un certain <b>code HTML</b>"
```

## Étape 2 - Les attributs

Ajouter un attribut à des éléments nouvellement créés.

### Les nouveaux mots-clés de l'étape 2

**En résumé** : `setAttribut`

```javascript
// Ajouter l'attribut unAttribut avec la valeur uneValeur à l'element
element.setAttribute(unAttribut, uneValeur);
```

## Étape 3 - Classes et styles

Les classes et les styles sont des attributs spéciaux : ils ont leurs propres mots-clés

### Les nouveaux mots-clés de l'étape 3

**En résumé** : `classList.add`, `style._propriete_` et `style.setProperty`

```javascript
// Ajouter la classe uneClasse à element.
element.classList.add(uneClass);

// Ajouter une propriété CSS à element.
element.style._propriete_ = "valeur de la propriété"

// Ajouter une propriété CSS à element. Autre syntaxe.
element.style.setProperty(unePropriete, uneValeur)
```

**Note** : On remplacera la portion `_propriete_` par une version _camel case_ du nom de la propriété. Par exemple, on mettra `element.style.fontSize = "12px";` (à la place de `font-size`)

## Étape 4 - Imbrication

On doit maintenant imbriquer des balises nouvellement créées dans des balises créées précédemment.

### Les nouveaux mots-clés de l'étape 4

Aucun

Il suffit de bien choisir l'élément auquel on applique le `appendChild`.

## Autres notions utiles

On peut combiner le `appendChild` et le `createElement` en une seule instruction:

```javascript
var h1 = app.appendChild(document.createElement("h1"));
```

On peut également utiliser `createTextNode` pour ajouter du texte à un élément:

```javascript
h1.appendChild(document.createTextNode("mon texte"));
```

On peut utiliser `setProperty` pour modifier le style. On utilise alors le nom habituel de la propriété CSS:

```javasctipt
h1.style.setProperty("background-color", "black");
```
