---
title: Footnote.footnote_type property
linktitle: footnote_type property
articleTitle: footnote_type property
second_title: Aspose.Words for Python
description: "Footnote.footnote_type property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /es/python-net/aspose.words.notes/footnote/footnote_type/
---

## Footnote.footnote_type property

Returns a value that specifies whether this is a footnote or endnote.


```python
@property
def footnote_type(self) -> aspose.words.notes.FootnoteType:
    ...

```

### Examples

Shows the difference between footnotes and endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# A continuación se presentan dos formas de adjuntar referencias numeradas al texto. Ambas referencias añadirán un
# pequeña marca de referencia en superíndice en la ubicación donde las insertamos.
# La marca de referencia, por defecto, es el número de índice de la referencia entre todas las referencias del documento.
# Cada referencia también creará una entrada, que tendrá la misma marca de referencia que en el texto del cuerpo.
# y texto de referencia, que pasaremos al método "InsertFootnote" del generador de documentos.
# 1 -  Una nota al pie, cuya entrada aparecerá en la misma página que el texto al que hace referencia:
builder.write('Footnote referenced main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text, will appear at the bottom of the page that contains the referenced text.')
# 2 -  Una nota final, cuya entrada aparecerá al final del documento:
builder.write('Endnote referenced main body text.')
endnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote text, will appear at the very end of the document.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.notes.FootnoteType.FOOTNOTE, footnote.footnote_type)
self.assertEqual(aw.notes.FootnoteType.ENDNOTE, endnote.footnote_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.FootnoteEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

