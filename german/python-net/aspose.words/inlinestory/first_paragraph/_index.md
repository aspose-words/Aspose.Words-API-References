---
title: InlineStory.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "InlineStory.first_paragraph property. Gets the first paragraph in the story."
type: docs
weight: 10
url: /de/python-net/aspose.words/inlinestory/first_paragraph/
---

## InlineStory.first_paragraph property

Gets the first paragraph in the story.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie Text hinzu und verweisen Sie darauf mit einer Fußnote. Diese Fußnote wird ein kleines hochgestelltes Referenzzeichen setzen
# nach dem Text, auf den sie verweist, und einen Eintrag unterhalb des Haupttextes am unteren Rand der Seite erzeugen.
# Dieser Eintrag wird das Referenzzeichen der Fußnote und den Referenztext enthalten,
# das wir an die "InsertFootnote"-Methode des Dokumenten‑Builders übergeben werden.
builder.write('Main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Wenn diese Eigenschaft auf "true" gesetzt ist, dann ist das Referenzzeichen unserer Fußnote
# ihr Index unter allen Fußnoten des Abschnitts.
# Dies ist die erste Fußnote, also wird das Referenzzeichen "1" sein.
self.assertTrue(footnote.is_auto)
# Wir können den Dokumenten‑Builder in die Fußnote verschieben, um deren Referenztext zu bearbeiten.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text.')
# Wir können ein benutzerdefiniertes Referenzzeichen festlegen, das die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# Ein Lesezeichen mit dem "IsAuto"-Flag, das auf true gesetzt ist, zeigt weiterhin seinen echten Index
# selbst wenn vorherige Lesezeichen benutzerdefinierte Referenzmarken anzeigen, wird die Referenzmarke dieses Lesezeichens eine "3" sein.
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
# In Microsoft Word können wir diesen Kommentar im Dokument-Body rechtsklicken, um ihn zu bearbeiten oder darauf zu antworten.
doc.save(ARTIFACTS_DIR + 'InlineStory.add_comment.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

