---
title: Document.endnote_options property
linktitle: endnote_options property
articleTitle: endnote_options property
second_title: Aspose.Words for Python
description: "Document.endnote_options property. Provides options that control numbering and positioning of endnotes in this document."
type: docs
weight: 120
url: /sv/python-net/aspose.words/document/endnote_options/
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

* module [aspose.words](../../)
* class [Document](../)

