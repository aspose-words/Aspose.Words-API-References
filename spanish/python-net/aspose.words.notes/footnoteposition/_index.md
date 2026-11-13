---
title: FootnotePosition enumeration
linktitle: FootnotePosition enumeration
articleTitle: FootnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnotePosition enumeration. Defines the footnote position."
type: docs
weight: 60
url: /es/python-net/aspose.words.notes/footnoteposition/
---

## FootnotePosition enumeration

Defines the footnote position.


### Members

| Name | Description |
| --- | --- |
| BOTTOM_OF_PAGE | Footnotes are output at the bottom of each page. |
| BENEATH_TEXT | Footnotes are output beneath text on each page. |

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una nota al pie es una forma de adjuntar una referencia o un comentario lateral al texto
# que no interfiere con el flujo del texto principal.
# Insertar una nota al pie agrega un pequeño símbolo de referencia en superíndice
# en el texto principal donde insertamos la nota al pie.
# Cada nota al pie también crea una entrada al final de la página, que consiste en un símbolo
# que coincide con el símbolo de referencia en el texto principal.
# El texto de referencia que pasamos al método "InsertFootnote" del generador de documentos.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# Podemos usar la propiedad "Position" para determinar dónde el documento colocará todas sus notas al pie.
# Si establecemos el valor de la propiedad "Position" a "FootnotePosition.BottomOfPage",
# cada nota al pie aparecerá al final de la página que contiene su marca de referencia. Este es el valor predeterminado.
# Si establecemos el valor de la propiedad "Position" a "FootnotePosition.BeneathText",
# cada nota al pie aparecerá al final del texto de la página que contiene su marca de referencia.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)

