---
title: EndnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "EndnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered endnotes."
type: docs
weight: 40
url: /sv/python-net/aspose.words.notes/endnoteoptions/start_number/
---

## EndnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered endnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [EndnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text.
# som inte stör huvudtextens flöde.
# Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
# i huvudtexten där vi infogar fotnoten/slutnoten.
# Varje fotnot/slutnot skapar också en post, som består av en symbol
# som matchar referenssymbolen i huvudtexten.
# Referenstexten som vi skickar till dokumentbyggarens metod "InsertEndnote".
# Fotnotsposter visas som standard längst ner på varje sida som innehåller
# deras referenssymboler, och slutnoter visas i slutet av dokumentet.
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
# Som standard är referenssymbolen för varje fotnot och slutnot dess index.
# bland alla dokumentets fotnoter/slutnoter. Varje dokument upprätthåller separata räknare.
# för fotnoter och för slutnoter, som båda börjar på 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Vi kan använda egenskapen "StartNumber" för att få dokumentet att
# börja en fotnot- eller slutnoträkning på ett annat nummer.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

