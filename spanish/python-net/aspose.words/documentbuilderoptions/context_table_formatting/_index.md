---
title: DocumentBuilderOptions.context_table_formatting property
linktitle: context_table_formatting property
articleTitle: context_table_formatting property
second_title: Aspose.Words for Python
description: "DocumentBuilderOptions.context_table_formatting property. True if the formatting applied to table content does not affect the formatting of the content that follows it"
type: docs
weight: 20
url: /es/python-net/aspose.words/documentbuilderoptions/context_table_formatting/
---

## DocumentBuilderOptions.context_table_formatting property

True if the formatting applied to table content does not affect the formatting of the content that follows it.
Default value is ``True``.



```python
@property
def context_table_formatting(self) -> bool:
    ...

@context_table_formatting.setter
def context_table_formatting(self, value: bool):
    ...

```

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

* module [aspose.words](../../)
* class [DocumentBuilderOptions](../)

