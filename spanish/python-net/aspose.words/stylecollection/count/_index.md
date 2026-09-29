---
title: StyleCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "StyleCollection.count property. Gets the number of styles in the collection."
type: docs
weight: 20
url: /es/python-net/aspose.words/stylecollection/count/
---

## StyleCollection.count property

Gets the number of styles in the collection.


```python
@property
def count(self) -> int:
    ...

```

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

