---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 100
url: /de/python-net/aspose.words.notes/footnotetype/
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
# Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, bei der die IsAuto-Eigenschaft standardmäßig auf "true" gesetzt ist,
# sodass das im Fließtext sichtbare Markierungszeichen automatisch auf "1" nummeriert wird,
# und die Fußnote am unteren Rand der Seite erscheint.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote comment regarding referenced text.')
# Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen,
# das anstelle der Nummer "2" verwendet wird und "IsAuto" auf false setzt.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote comment regarding referenced text.', reference_mark='CustomMark')
# Fußnoten erscheinen immer am unteren Rand des referenzierten Textes,
# sodass dieser Seitenumbruch die Fußnote nicht beeinflusst.
# Andererseits befinden sich Endnoten immer am Ende des Dokuments
# sodass dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertFootnote.docx')
```

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

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

