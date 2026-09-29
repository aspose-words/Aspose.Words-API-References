---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /es/python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```python
@property
def break_is_style_separator(self) -> bool:
    ...

```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_table_of_contents('\\o \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Inserte un párrafo con un estilo que el TOC reconocerá como una entrada.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
# Ambas cadenas están en el mismo párrafo y, por lo tanto, aparecerán en la misma entrada del TOC.
builder.write('Heading 1. ')
builder.write('Will appear in the TOC. ')
# Si insertamos un separador de estilo, podemos escribir más texto en el mismo párrafo
# y usar un estilo diferente sin que aparezca en el índice.
# Si usamos un estilo de tipo encabezado después del separador, podemos generar múltiples entradas en el índice a partir de una sola línea de texto del documento.
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")
self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.BreakIsStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

