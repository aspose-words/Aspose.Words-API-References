---
title: StyleCollection indexer
linktitle: StyleCollection indexer
articleTitle: StyleCollection indexer
second_title: Aspose.Words for Python
description: "StyleCollection indexer. Gets a style by index."
type: docs
weight: 10
url: /es/python-net/aspose.words/stylecollection/__getitem__/
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
# Establecer parámetros predeterminados para los nuevos estilos que podamos añadir más tarde a esta colección.
styles.default_font.name = 'Courier New'
# Si añadimos un estilo de "StyleType.Paragraph", la colección aplicará los valores de
# su propiedad "DefaultParagraphFormat" al "ParagraphFormat" del estilo.
styles.default_paragraph_format.first_line_indent = 15
# Añade un estilo y luego verifica que tenga la configuración predeterminada.
styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
self.assertEqual('Courier New', styles[4].font.name)
self.assertEqual(15, styles.get_by_name('MyStyle').paragraph_format.first_line_indent)
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

