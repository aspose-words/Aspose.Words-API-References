---
title: DocumentBuilderOptions class
linktitle: DocumentBuilderOptions class
articleTitle: DocumentBuilderOptions class
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilderOptions class. Allows to specify additional options for the document building process."
type: docs
weight: 320
url: /es/python-net/aspose.words/documentbuilderoptions/
---

## DocumentBuilderOptions class

Allows to specify additional options for the document building process.


### Constructors
| Name | Description |
| --- | --- |
| [DocumentBuilderOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [context_table_formatting](./context_table_formatting/) | True if the formatting applied to table content does not affect the formatting of the content that follows it. Default value is ``True``. |
| [design_mode](./design_mode/) | Corresponds to Design Mode in Microsoft Word. |

### Examples

Shows how to ignore table formatting for content after.

```python
doc = aw.Document()
builder_options = aw.DocumentBuilderOptions()
builder_options.context_table_formatting = True
builder = aw.DocumentBuilder(doc=doc, options=builder_options)
# Agrega contenido antes de la tabla.
# El tamaño de fuente predeterminado es 12.
builder.writeln('Font size 12 here.')
builder.start_table()
builder.insert_cell()
# Cambia el tamaño de fuente dentro de la tabla.
builder.font.size = 5
builder.write('Font size 5 here')
builder.insert_cell()
builder.write('Font size 5 here')
builder.end_row()
builder.end_table()
# Si ContextTableFormatting es verdadero, entonces el formato de tabla no se aplica al contenido posterior.
# Si ContextTableFormatting es falso, entonces el formato de tabla se aplica al contenido posterior.
builder.writeln('Font size 12 here.')
doc.save(file_name=ARTIFACTS_DIR + 'Table.ContextTableFormatting.docx')
```

### See Also

* module [aspose.words](../)

