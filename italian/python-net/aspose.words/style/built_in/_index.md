---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /it/python-net/aspose.words/style/built_in/
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
# Quando creiamo un documento usando Microsoft Word, o programmaticamente usando Aspose.Words,
# il documento verrà fornito con una raccolta di stili da applicare al suo testo per modificarne l'aspetto.
# Possiamo accedere a questi stili incorporati tramite la raccolta "Styles" del documento.
# Tutti questi stili avranno il flag "BuiltIn" impostato su "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Crea uno stile personalizzato e aggiungilo alla raccolta.
# Stili personalizzati come questo avranno il flag "BuiltIn" impostato su "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

