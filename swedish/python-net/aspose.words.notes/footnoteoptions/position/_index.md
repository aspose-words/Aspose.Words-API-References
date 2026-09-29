---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /sv/python-net/aspose.words.notes/footnoteoptions/position/
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
# En fotnot är ett sätt att bifoga en referens eller en sidokommentar till text
# som inte stör huvudtextens flöde.
# Att infoga en fotnot lägger till en liten upphöjd referenssymbol
# i huvudtexten där vi infogar fotnoten.
# Varje fotnot skapar också en post längst ner på sidan, bestående av en symbol.
# som matchar referenssymbolen i huvudtexten.
# Referenstexten som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# Vi kan använda egenskapen "Position" för att bestämma var dokumentet kommer att placera alla sina fotnoter.
# Om vi sätter värdet på egenskapen "Position" till "FootnotePosition.BottomOfPage",
# kommer varje fotnot att visas längst ner på sidan som innehåller dess referensmärke. Detta är standardvärdet.
# Om vi sätter värdet på egenskapen "Position" till "FootnotePosition.BeneathText",
# kommer varje fotnot att visas i slutet av sidans text som innehåller dess referensmärke.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

