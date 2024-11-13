---
title: FootnoteNumberingRule enumeration
linktitle: FootnoteNumberingRule enumeration
articleTitle: FootnoteNumberingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteNumberingRule enumeration. Determines when automatic footnote or endnote numbering restarts."
type: docs
weight: 40
url: /python-net/aspose.words.notes/footnotenumberingrule/
---

## FootnoteNumberingRule enumeration

Determines when automatic footnote or endnote numbering restarts.


### Members

| Name | Description |
| --- | --- |
| CONTINUOUS | Numbering continuous throughout the document. |
| RESTART_SECTION | Numbering restarts at each section. |
| RESTART_PAGE | Numbering restarts at each page. Valid for footnotes only. |
| DEFAULT | Equals [FootnoteNumberingRule.CONTINUOUS](./#CONTINUOUS). |

### Examples

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Footnotes and endnotes are a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting a footnote/endnote adds a small superscript reference symbol
# at the main body text where we insert the footnote/endnote.
# Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
# symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
# Footnote entries, by default, show up at the bottom of each page that contains
# their reference symbols, and endnotes show up at the end of the document.
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
# By default, the reference symbol for each footnote and endnote is its index
# among all the document's footnotes/endnotes. Each document maintains separate counts
# for footnotes and endnotes and does not restart these counts at any point.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# We can use the "RestartRule" property to get the document to restart
# the footnote/endnote counts at a new page or section.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)

