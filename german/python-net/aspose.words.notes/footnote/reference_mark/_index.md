---
title: Footnote.reference_mark property
linktitle: reference_mark property
articleTitle: reference_mark property
second_title: Aspose.Words for Python
description: "Footnote.reference_mark property. Gets/sets custom reference mark to be used for this footnote"
type: docs
weight: 60
url: /de/python-net/aspose.words.notes/footnote/reference_mark/
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

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

