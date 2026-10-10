---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /es/python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte algún texto y márquelo con una nota al pie con la propiedad IsAuto establecida en "true" por defecto,
# de modo que el marcador visto en el texto principal se numerará automáticamente como "1",
# y la nota al pie aparecerá al final de la página.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Inserte más texto y márquelo con una nota final con una marca de referencia personalizada,
# que se usará en lugar del número "2" y establecerá "IsAuto" a false.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Las notas al pie siempre aparecen al final de su texto referenciado,
# por lo que este salto de página no afectará a la nota al pie.
# Por otro lado, las notas finales siempre están al final del documento
# de modo que este salto de página empujará la nota final a la página siguiente.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Agregue texto y refiérencielo con una nota al pie. Esta nota al pie colocará una pequeña referencia en superíndice
# después del texto al que hace referencia y creará una entrada debajo del texto principal al final de la página.
# Esta entrada contendrá la marca de referencia de la nota al pie y el texto de referencia,
# que pasaremos al método "InsertFootnote" del generador de documentos.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Si esta propiedad se establece en "true", entonces la marca de referencia de nuestra nota al pie
# será su índice entre todas las notas al pie de la sección.
# Esta es la primera nota al pie, por lo que la marca de referencia será "1".
self.assertTrue(footnote.is_auto)
# Podemos mover el generador de documentos dentro de la nota al pie para editar su texto de referencia.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Podemos establecer una marca de referencia personalizada que la nota al pie usará en lugar de su número de índice.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Un marcador con la bandera "IsAuto" establecida en true aún mostrará su índice real
# incluso si los marcadores anteriores muestran marcas de referencia personalizadas, la marca de referencia de este marcador será un "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.AddFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

