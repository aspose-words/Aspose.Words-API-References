---
title: StyleCollection.default_font property
linktitle: default_font property
articleTitle: default_font property
second_title: Aspose.Words for Python
description: "StyleCollection.default_font property. Gets document default text formatting."
type: docs
weight: 30
url: /es/python-net/aspose.words/stylecollection/default_font/
---

## StyleCollection.default_font property

Gets document default text formatting.


```python
@property
def default_font(self) -> aspose.words.Font:
    ...

```

### Remarks

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ([LoadFormat.DOCX](../../loadformat/#DOCX)) only.
Earlier document formats have limited support for this feature and only font names can be stored.




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

