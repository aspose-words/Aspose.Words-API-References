---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /de/python-net/aspose.words/style/built_in/
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
# Wenn wir ein Dokument mit Microsoft Word oder programmgesteuert mit Aspose.Words erstellen,
# wird das Dokument mit einer Sammlung von Formatvorlagen geliefert, die auf seinen Text angewendet werden können, um dessen Aussehen zu ändern.
# Wir können auf diese integrierten Formatvorlagen über die "Styles"-Sammlung des Dokuments zugreifen.
# Alle diese Formatvorlagen haben das "BuiltIn"-Flag auf "true" gesetzt.
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# Erstellen Sie eine benutzerdefinierte Formatvorlage und fügen Sie sie der Sammlung hinzu.
# Benutzerdefinierte Formatvorlagen wie diese haben das "BuiltIn"-Flag auf "false" gesetzt.
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

