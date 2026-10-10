---
title: FootnotePosition enumeration
linktitle: FootnotePosition enumeration
articleTitle: FootnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnotePosition enumeration. Defines the footnote position."
type: docs
weight: 60
url: /de/python-net/aspose.words.notes/footnoteposition/
---

## FootnotePosition enumeration

Defines the footnote position.


### Members

| Name | Description |
| --- | --- |
| BOTTOM_OF_PAGE | Footnotes are output at the bottom of each page. |
| BENEATH_TEXT | Footnotes are output beneath text on each page. |

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Eine Fußnote ist eine Möglichkeit, einen Verweis oder einen Randkommentar an Text anzuhängen.
# der den Fluss des Haupttextes nicht stört.
# Das Einfügen einer Fußnote fügt ein kleines hochgestelltes Referenzsymbol hinzu.
# im Fließtext, wo wir die Fußnote einfügen.
# Jede Fußnote erstellt außerdem einen Eintrag am unteren Rand der Seite, bestehend aus einem Symbol
# das dem Verweissymbol im Haupttext entspricht.
# Der Referenztext, den wir an die Methode "InsertFootnote" des Dokumenten‑Builders übergeben.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# Wir können die Eigenschaft "Position" verwenden, um zu bestimmen, wo das Dokument alle seine Fußnoten platziert.
# Wenn wir den Wert der Eigenschaft "Position" auf "FootnotePosition.BottomOfPage" setzen,
# wird jede Fußnote am unteren Rand der Seite angezeigt, die ihre Referenzmarke enthält. Dies ist der Standardwert.
# Wenn wir den Wert der Eigenschaft "Position" auf "FootnotePosition.BeneathText" setzen,
# wird jede Fußnote am Ende des Textes der Seite angezeigt, die ihre Referenzmarke enthält.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)

