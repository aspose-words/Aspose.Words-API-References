---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /sv/python-net/aspose.words/style/built_in/
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
# När vi skapar ett dokument med Microsoft Word, eller programmässigt med Aspose.Words,
# kommer dokumentet med en samling stilar som kan tillämpas på dess text för att ändra dess utseende.
# Vi kan komma åt dessa inbyggda stilar via dokumentets "Styles"-samling.
# Dessa stilar kommer alla ha flaggan "BuiltIn" satt till "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Skapa en anpassad stil och lägg till den i samlingen.
# Anpassade stilar som denna kommer ha flaggan "BuiltIn" satt till "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

