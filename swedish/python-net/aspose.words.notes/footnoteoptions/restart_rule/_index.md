---
title: FootnoteOptions.restart_rule property
linktitle: restart_rule property
articleTitle: restart_rule property
second_title: Aspose.Words for Python
description: "FootnoteOptions.restart_rule property. Determines when automatic numbering restarts."
type: docs
weight: 40
url: /sv/python-net/aspose.words.notes/footnoteoptions/restart_rule/
---

## FootnoteOptions.restart_rule property

Determines when automatic numbering restarts.


```python
@property
def restart_rule(self) -> aspose.words.notes.FootnoteNumberingRule:
    ...

@restart_rule.setter
def restart_rule(self, value: aspose.words.notes.FootnoteNumberingRule):
    ...

```

### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

