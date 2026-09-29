---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /sv/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# En slutnot är ett sätt att bifoga en referens eller en sidokommentar till text
# som inte stör huvudtextens flöde.
# Att infoga en slutnot lägger till en liten upphöjd referenssymbol
# i huvudtexten där vi infogar slutnoten.
# Varje slutnot skapar också ett post i slutet av dokumentet, bestående av en symbol
# som matchar referenssymbolen i huvudtexten.
# Referenstexten som vi skickar till dokumentbyggarens metod "InsertEndnote".
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Vi kan använda egenskapen "Position" för att bestämma var dokumentet placerar alla sina slutnoter.
# Om vi sätter värdet på egenskapen "Position" till "EndnotePosition.EndOfDocument",
# kommer varje fotnot att visas i en samling i slutet av dokumentet. Detta är standardvärdet.
# Om vi sätter värdet på egenskapen "Position" till "EndnotePosition.EndOfSection",
# varje fotnot kommer att visas i en samling i slutet av avsnittet vars text innehåller slutnotens referensmärke.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

