---
title: Footnote.reference_mark property
linktitle: reference_mark property
articleTitle: reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.reference_mark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /es/python-net/aspose.words.notes/footnote/reference_mark/
---

## Footnote.reference_mark property

Gets/sets custom reference mark to be used for this footnote.
Default value is **empty string** (), meaning auto-numbered footnotes are used.



```python
@property
def reference_mark(self) -> str:
    ...

@reference_mark.setter
def reference_mark(self, value: str):
    ...

```

### Remarks

If this property is set to **empty string** () or ``None``, then [Footnote.is_auto](../is_auto/) property will automatically be set to ``True``, 
if set to anything else then [Footnote.is_auto](../is_auto/) will be set to ``False``.


RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.




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

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

