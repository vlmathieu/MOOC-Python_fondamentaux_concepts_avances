---
jupytext:
  cell_metadata_filter: all
  notebook_metadata_filter: all,-language_info,-toc,-jupytext.text_representation.jupytext_version,-jupytext.text_representation.format_version
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
notebookname: module this
version: '3.0'
---

<div class="licence">
<span>Licence CC BY-NC-ND</span>
<span>Thierry Parmentelat &amp; Arnaud Legout</span>
<span><img src="media/both-logos-small-alpha.png" /></span>
</div>

+++

# Décoder le module `this`

+++

## Exercice - niveau avancé

+++

### Le module `this` et le *Zen de Python*

+++

Nous avons déjà eu l'occasion de parler du *Zen de Python* ; on peut lire ce texte en important le module `this` comme ceci

```{code-cell}
import this
```

Il suit du cours qu'une fois cet import effectué nous avons accès à une variable `this`, de type module :

```{code-cell}
this
```

### But de l'exercice

```{code-cell}
# chargement de l'exercice
from corrections.exo_decode_zen import exo_decode_zen
```

Constatant que le texte du manifeste doit se trouver quelque part dans le module, le but de l'exercice est de deviner le contenu du module, et d'écrire une fonction `decode_zen`, qui retourne le texte du manifeste.

+++

### Indices

+++

Cet exercice peut paraître un peu déconcertant ; voici quelques indices optionnels :

```{code-cell}
# on rappelle que dir() renvoie les noms des attributs 
# accessibles à partir de l'objet
dir(this)
```

Vous pouvez ignorer `this.c` et `this.i`, les deux autres variables du module sont importantes pour nous.

```{code-cell}
# ici on calcule le résultat attendu
resultat = exo_decode_zen.resultat(this)
```

Ceci devrait vous donner une idée de comment utiliser une des deux variables du module :

```{code-cell}
# ces deux quantités sont égales
len(this.s) == len(resultat)
```

À quoi peut bien servir l'autre variable ?

```{code-cell}
# se pourrait-il que d agisse comme un code simple ?
this.d[this.s[0]] == resultat[0]
```

Le texte comporte certes des caractères alphabétiques

```{code-cell}
# si on ignore les accents, 
# il y a 26 caractères minuscules
# et 26 caractères majuscules
len(this.d)
```

mais pas seulement ; les autres sont préservés.

+++

### À vous de jouer

```{code-cell}
def decode_zen(this):
    "<votre code>"
```

### Correction

```{code-cell}
exo_decode_zen.correction(decode_zen)
```