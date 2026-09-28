---
title: FootnoteNumberingRule enumeration
linktitle: FootnoteNumberingRule enumeration
articleTitle: FootnoteNumberingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteNumberingRule enumeration. Determines when automatic footnote or endnote numbering restarts."
type: docs
weight: 40
url: /de/python-net/aspose.words.notes/footnotenumberingrule/
---

## FootnoteNumberingRule enumeration

Determines when automatic footnote or endnote numbering restarts.


### Members

| Name | Description |
| --- | --- |
| CONTINUOUS | Numbering continuous throughout the document. |
| RESTART_SECTION | Numbering restarts at each section. |
| RESTART_PAGE | Numbering restarts at each page. Valid for footnotes only. |
| DEFAULT | Equals [FootnoteNumberingRule.CONTINUOUS](./#CONTINUOUS). |

### Examples

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen.
# der den Fluss des Haupttextes nicht stört.
# Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu.
# im Fließtext, wo wir die Fußnote/Endnote einfügen.
# Jede Fußnote/Endnote erstellt außerdem einen Eintrag, der aus einem Symbol besteht, das dem Referenz
# Symbol im Fließtext entspricht. Der Referenztext, den wir an die Methode "InsertEndnote" des Dokumenten‑Builders übergeben.
# Fußnoteneinträge werden standardmäßig am unteren Rand jeder Seite angezeigt, die
# ihre Referenzsymbole enthalten, und Endnoten werden am Ende des Dokuments angezeigt.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
# unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument führt separate Zähler
# für Fußnoten und Endnoten und setzt diese Zähler zu keinem Zeitpunkt zurück.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Wir können die "RestartRule"-Eigenschaft verwenden, um das Dokument neu zu starten
# die Fußnote/Endnote-Zählungen beginnen auf einer neuen Seite oder in einem Abschnitt.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)

