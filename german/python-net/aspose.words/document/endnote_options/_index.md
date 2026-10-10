---
title: Document.endnote_options property
linktitle: endnote_options property
articleTitle: endnote_options property
second_title: Aspose.Words for Python
description: "Document.endnote_options property. Provides options that control numbering and positioning of endnotes in this document."
type: docs
weight: 120
url: /de/python-net/aspose.words/document/endnote_options/
---

## Document.endnote_options property

Provides options that control numbering and positioning of endnotes in this document.


```python
@property
def endnote_options(self) -> aspose.words.notes.EndnoteOptions:
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Eine Endnote ist eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen
# der den Fluss des Haupttextes nicht stört.
# Das Einfügen einer Endnote fügt ein kleines hochgestelltes Verweissymbol hinzu
# im Haupttext an der Stelle, an der wir die Endnote einfügen.
# Jede Endnote erzeugt außerdem einen Eintrag am Ende des Dokuments, bestehend aus einem Symbol
# das dem Verweissymbol im Haupttext entspricht.
# Der Referenztext, den wir an die "InsertEndnote"-Methode des Dokumenten‑Builders übergeben.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Wir können die Eigenschaft "Position" verwenden, um zu bestimmen, wo das Dokument alle seine Endnoten platziert.
# Wenn wir den Wert der Eigenschaft "Position" auf "EndnotePosition.EndOfDocument" setzen,
# wird jede Fußnote in einer Sammlung am Ende des Dokuments angezeigt. Dies ist der Standardwert.
# Wenn wir den Wert der Eigenschaft "Position" auf "EndnotePosition.EndOfSection" setzen,
# Jede Fußnote wird in einer Sammlung am Ende des Abschnitts angezeigt, dessen Text die Referenzmarke der Endnote enthält.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

