---
title: DocumentBuilder.insert_table_of_contents method
linktitle: insert_table_of_contents method
articleTitle: insert_table_of_contents method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_table_of_contents method. Inserts a TOC (table of contents) field into the document."
type: docs
weight: 500
url: /es/python-net/aspose.words/documentbuilder/insert_table_of_contents/
---

## insert_table_of_contents(switches) {#str}

Inserts a TOC (table of contents) field into the document.


```python
def insert_table_of_contents(self, switches: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| switches | str | The TOC field switches. |

### Remarks

This method inserts a TOC (table of contents) field into the document at
the current position.

A table of contents in a Word document can be built in a number of ways
and formatted using a variety of options. The way the table is built and
displayed by Microsoft Word is controlled by the field switches.

The easiest way to specify the switches is to insert and configure a table of
contents into a Word document using the Insert-\>Reference-\>Index and Tables menu,
then switch display of field codes on to see the switches. You can press Alt+F9 in
Microsoft Word to toggle display of field codes on or off.

For example, after creating a table of contents, the following field is inserted
into the document: **{ TOC \\o "1-3" \\h \\z \\u }**.
You can copy **\\o "1-3" \\h \\z \\u** and use it as the switches parameter.

Note that [DocumentBuilder.insert_table_of_contents()](./#str) will only insert a TOC field, but
will not actually build the table of contents. The table of contents is built by
Microsoft Word when the field is updated.

If you insert a table of contents using this method and then open the file
in Microsoft Word, you will not see the table of contents because the TOC field
has not yet been updated.

In Microsoft Word, fields are not automatically updated when a document is opened,
but you can update fields in a document at any time by pressing F9.




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
* class [DocumentBuilder](../)

