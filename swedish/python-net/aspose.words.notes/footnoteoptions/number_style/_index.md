---
title: FootnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "FootnoteOptions.number_style property. Specifies the number format for automatically numbered footnotes."
type: docs
weight: 20
url: /sv/python-net/aspose.words.notes/footnoteoptions/number_style/
---

## FootnoteOptions.number_style property

Specifies the number format for automatically numbered footnotes.


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
# Fotnoter och slutnoter är ett sätt att bifoga en referens eller en sidokommentar till text.
# som inte stör huvudtextens flöde.
# Att infoga en fotnot/slutnot lägger till en liten upphöjd referenssymbol
# i huvudtexten där vi infogar fotnoten/slutnoten.
# Varje fotnot/slutnot skapar också en post, som består av en symbol som matchar referensen
# symbol i huvudtexten. Referenstexten som vi skickar till dokumentbyggarens "InsertEndnote"-metod.
# Fotnotsposter visas som standard längst ner på varje sida som innehåller
# deras referenssymboler, och slutnoter visas i slutet av dokumentet.
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
# Som standard är referenssymbolen för varje fotnot och slutnot dess index.
# bland alla dokumentets fotnoter/slutnoter. Varje dokument upprätthåller separata räknare.
# för fotnoter och för slutnoter. Som standard visar fotnoter sina nummer med arabiska siffror,
# och slutnoter visar sina nummer med gemena romerska siffror.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# Vi kan använda egenskapen "NumberStyle" för att tillämpa anpassade numreringsstilar på fotnoter och slutnoter.
# Detta kommer inte att påverka fotnoter/slutnoter med anpassade referensmärken.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

