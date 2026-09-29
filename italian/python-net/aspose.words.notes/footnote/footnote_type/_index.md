---
title: Footnote.footnote_type property
linktitle: footnote_type property
articleTitle: footnote_type property
second_title: Aspose.Words for Python
description: "Footnote.footnote_type property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /it/python-net/aspose.words.notes/footnote/footnote_type/
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
# Di seguito sono riportati due modi per aggiungere riferimenti numerati al testo. Entrambi questi riferimenti aggiungeranno un
# piccolo segno di riferimento in apice nella posizione in cui li inseriamo.
# Il segno di riferimento, per impostazione predefinita, è il numero indice del riferimento tra tutti i riferimenti nel documento.
# Ogni riferimento creerà anche una voce, che avrà lo stesso segno di riferimento del testo principale.
# e il testo di riferimento, che passeremo al metodo "InsertFootnote" del costruttore di documenti.
# 1 -  Una nota a piè di pagina, la cui voce apparirà nella stessa pagina del testo a cui fa riferimento:
builder.write('Footnote referenced main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text, will appear at the bottom of the page that contains the referenced text.')
# 2 -  Una nota finale, la cui voce apparirà alla fine del documento:
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

