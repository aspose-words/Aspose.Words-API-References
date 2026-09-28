---
title: EndnotePosition enumeration
linktitle: EndnotePosition enumeration
articleTitle: EndnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.EndnotePosition enumeration. Defines the endnote position."
type: docs
weight: 20
url: /de/python-net/aspose.words.notes/endnoteposition/
---

## EndnotePosition enumeration

Defines the endnote position.


### Members

| Name | Description |
| --- | --- |
| END_OF_SECTION | Endnotes are output at the end of the section. |
| END_OF_DOCUMENT | Endnotes are output at the end of the document. |

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

### See Also

* module [aspose.words.notes](../)
* class [EndnoteOptions](../endnoteoptions/)

