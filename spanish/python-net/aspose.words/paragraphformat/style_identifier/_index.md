---
title: ParagraphFormat.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "ParagraphFormat.style_identifier property. Gets or sets the locale independent style identifier of the paragraph style applied to this formatting."
type: docs
weight: 360
url: /es/python-net/aspose.words/paragraphformat/style_identifier/
---

## ParagraphFormat.style_identifier property

Gets or sets the locale independent style identifier of the paragraph style applied to this formatting.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

@style_identifier.setter
def style_identifier(self, value: aspose.words.StyleIdentifier):
    ...

```

### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte una tabla de contenido para la primera página del documento.
# Configure la tabla para que incluya párrafos con encabezados de niveles del 1 al 3.
# Además, configure sus entradas para que sean hipervínculos que nos lleven
# a la ubicación del encabezado al hacer clic izquierdo en Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Llena la tabla de contenido añadiendo párrafos con estilos de encabezado.
# Cada encabezado de este tipo con un nivel entre 1 y 3 creará una entrada en la tabla.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Una tabla de contenido es un campo de un tipo que necesita actualizarse para mostrar un resultado actualizado.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

