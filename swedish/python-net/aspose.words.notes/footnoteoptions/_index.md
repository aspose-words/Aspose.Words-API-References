---
title: FootnoteOptions class
linktitle: FootnoteOptions class
articleTitle: FootnoteOptions class
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteOptions class. Represents the footnote numbering options for a document or section"
type: docs
weight: 50
url: /sv/python-net/aspose.words.notes/footnoteoptions/
---

## FootnoteOptions class

Represents the footnote numbering options for a document or section.
To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/python-net/working-with-footnote-and-endnote/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [columns](./columns/) | Specifies the number of columns with which the footnotes area is formatted. |
| [number_style](./number_style/) | Specifies the number format for automatically numbered footnotes. |
| [position](./position/) | Specifies the footnotes position. |
| [restart_rule](./restart_rule/) | Determines when automatic numbering restarts. |
| [start_number](./start_number/) | Specifies the starting number or character for the first automatically numbered footnotes. |

### Examples

Shows how to split the footnote section into a given number of columns.

```python
doc = aw.Document(file_name=MY_DIR + 'Footnotes and endnotes.docx')
doc.footnote_options.columns = 2
doc.save(file_name=ARTIFACTS_DIR + 'Document.FootnoteColumns.docx')
```

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

Shows how to restart footnote/endnote numbering at certain places in the document.

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
# Som standard är referenssymbolen för varje fotnot och slutnot dess index.
# bland alla dokumentets fotnoter/slutnoter. Varje dokument upprätthåller separata räknare.
# för fotnoter och slutnoter och återställer inte dessa räknare någon gång.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Vi kan använda egenskapen "RestartRule" för att få dokumentet att starta om
# Fotnot-/slutnoträkningen sker på en ny sida eller sektion.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

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

* module [aspose.words.notes](../)
* property [Document.footnote_options](../../aspose.words/document/footnote_options/)
* property [PageSetup.footnote_options](../../aspose.words/pagesetup/footnote_options/)

