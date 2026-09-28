---
title: Footnote.footnote_type property
linktitle: footnote_type property
articleTitle: footnote_type property
second_title: Aspose.Words for Python
description: "Footnote.footnote_type property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /de/python-net/aspose.words.notes/footnote/footnote_type/
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
# Unten sind zwei Methoden aufgeführt, um nummerierte Verweise zum Text hinzuzufügen. Beide Verweise werden ein
# kleines hochgestelltes Referenzzeichen an der Stelle, an der wir sie einfügen.
# Das Referenzzeichen ist standardmäßig die Indexnummer der Referenz unter allen Referenzen im Dokument.
# Jede Referenz erstellt außerdem einen Eintrag, der dasselbe Referenzzeichen wie im Fließtext hat
# und Referenztext, den wir an die Methode "InsertFootnote" des Dokumenten‑Builders übergeben.
# 1 -  Eine Fußnote, deren Eintrag auf derselben Seite wie der referenzierte Text erscheint:
builder.write('Footnote referenced main body text.')
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote text, will appear at the bottom of the page that contains the referenced text.')
# 2 -  Eine Endnote, deren Eintrag am Ende des Dokuments erscheint:
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

