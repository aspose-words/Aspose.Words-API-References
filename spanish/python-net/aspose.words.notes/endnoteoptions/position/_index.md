---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /es/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una nota al final es una forma de adjuntar una referencia o un comentario lateral al texto
# que no interfiere con el flujo del texto principal.
# Insertar una nota al final agrega un pequeño símbolo de referencia en superíndice
# en el texto principal donde insertamos la nota al final.
# Cada nota al final también crea una entrada al final del documento, que consiste en un símbolo
# que coincide con el símbolo de referencia en el texto principal.
# El texto de referencia que pasamos al método "InsertEndnote" del constructor de documentos.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Podemos usar la propiedad "Position" para determinar dónde el documento colocará todas sus notas al final.
# Si establecemos el valor de la propiedad "Position" a "EndnotePosition.EndOfDocument",
# Cada nota al pie aparecerá en una colección al final del documento. Este es el valor predeterminado.
# Si establecemos el valor de la propiedad "Position" a "EndnotePosition.EndOfSection",
# cada nota al pie aparecerá en una colección al final de la sección cuyo texto contiene la marca de referencia de la nota final.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

