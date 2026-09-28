---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /fr/python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


```python
@property
def built_in(self) -> bool:
    ...

```

### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()
# Lorsque nous créons un document avec Microsoft Word, ou de manière programmatique avec Aspose.Words,
# le document sera fourni avec une collection de styles à appliquer à son texte pour modifier son apparence.
# Nous pouvons accéder à ces styles intégrés via la collection "Styles" du document.
# Tous ces styles auront le drapeau "BuiltIn" défini sur "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Créez un style personnalisé et ajoutez-le à la collection.
# Les styles personnalisés comme celui-ci auront le drapeau "BuiltIn" défini sur "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

