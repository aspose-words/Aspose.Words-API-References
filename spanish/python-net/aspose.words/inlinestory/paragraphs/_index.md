---
title: InlineStory.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "InlineStory.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 80
url: /es/python-net/aspose.words/inlinestory/paragraphs/
---

## InlineStory.paragraphs property

Gets a collection of paragraphs that are immediate children of the story.


```python
@property
def paragraphs(self) -> aspose.words.ParagraphCollection:
    ...

```

### Examples

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

Shows how to add a comment to a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
comment = aw.Comment(doc, 'John Doe', 'JD', date.today())
builder.current_paragraph.append_child(comment)
builder.move_to(comment.append_child(aw.Paragraph(doc)))
builder.write('Comment text.')
self.assertEqual(date.today(), comment.date_time.date())
# En Microsoft Word, podemos hacer clic derecho en este comentario en el cuerpo del documento para editarlo o responderlo.
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

