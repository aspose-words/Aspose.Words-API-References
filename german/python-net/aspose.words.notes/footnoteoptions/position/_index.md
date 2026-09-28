---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /de/python-net/aspose.words.notes/footnoteoptions/position/
---

## FootnoteOptions.position property

Specifies the footnotes position.


```python
@property
def position(self) -> aspose.words.notes.FootnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.FootnotePosition):
    ...

```

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

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

