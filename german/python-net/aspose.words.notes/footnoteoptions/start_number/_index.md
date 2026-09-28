---
title: FootnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "FootnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered footnotes."
type: docs
weight: 50
url: /de/python-net/aspose.words.notes/footnoteoptions/start_number/
---

## FootnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered footnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [FootnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fußnoten und Endnoten sind eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen.
# der den Fluss des Haupttextes nicht stört.
# Das Einfügen einer Fußnote/Endnote fügt ein kleines hochgestelltes Referenzsymbol hinzu.
# im Fließtext, wo wir die Fußnote/Endnote einfügen.
# Jede Fußnote/Endnote erstellt ebenfalls einen Eintrag, der aus einem Symbol besteht
# das dem Verweissymbol im Haupttext entspricht.
# Der Referenztext, den wir an die "InsertEndnote"-Methode des Dokumenten‑Builders übergeben.
# Fußnoteneinträge werden standardmäßig am unteren Rand jeder Seite angezeigt, die
# ihre Referenzsymbole enthalten, und Endnoten werden am Ende des Dokuments angezeigt.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
# unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument führt separate Zähler
# für Fußnoten und Endnoten, die beide bei 1 beginnen.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Wir können die "StartNumber"-Eigenschaft verwenden, um das Dokument zu
# beginnen, dass die Fußnote- oder Endnote-Zählung bei einer anderen Nummer startet.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

