---
title: EndnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "EndnoteOptions.number_style property. Specifies the number format for automatically numbered endnotes."
type: docs
weight: 10
url: /de/python-net/aspose.words.notes/endnoteoptions/number_style/
---

## EndnoteOptions.number_style property

Specifies the number format for automatically numbered endnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

Shows how to change the number style of footnote/endnote reference marks.

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
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# Standardmäßig ist das Referenzsymbol für jede Fußnote und Endnote ihr Index
# unter allen Fußnoten/Endnoten des Dokuments. Jedes Dokument führt separate Zähler
# für Fußnoten und für Endnoten. Standardmäßig zeigen Fußnoten ihre Nummern mit arabischen Ziffern an,
# und Endnoten zeigen ihre Nummern in kleinen römischen Ziffern an.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# Wir können die Eigenschaft "NumberStyle" verwenden, um benutzerdefinierte Nummerierungsstile auf Fußnoten und Endnoten anzuwenden.
# Dies wirkt sich nicht auf Fußnoten/Endnoten mit benutzerdefinierten Referenzmarken aus.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

