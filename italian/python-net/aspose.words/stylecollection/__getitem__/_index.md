---
title: StyleCollection indexer
linktitle: StyleCollection indexer
articleTitle: StyleCollection indexer
second_title: Aspose.Words for Python
description: "StyleCollection indexer. Gets a style by index."
type: docs
weight: 10
url: /it/python-net/aspose.words/stylecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a style by index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to add a Style to a document's styles collection.

```python
doc = aw.Document()
styles = doc.styles
# Imposta i parametri predefiniti per i nuovi stili che potremmo aggiungere in seguito a questa raccolta.
styles.default_font.name = 'Courier New'
# Se aggiungiamo uno stile di tipo "StyleType.Paragraph", la raccolta applicherà i valori di
# la sua proprietà "DefaultParagraphFormat" allo "ParagraphFormat" dello stile.
styles.default_paragraph_format.first_line_indent = 15
# Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

