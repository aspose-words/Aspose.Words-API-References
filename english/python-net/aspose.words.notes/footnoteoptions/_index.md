---
title: FootnoteOptions class
linktitle: FootnoteOptions class
articleTitle: FootnoteOptions class
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteOptions class. Represents the footnote numbering options for a document or section"
type: docs
weight: 50
url: /python-net/aspose.words.notes/footnoteoptions/
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
doc = aw.Document(MY_DIR + "Footnotes and endnotes.docx")

doc.footnote_options.columns = 2
doc.save(ARTIFACTS_DIR + "Document.footnote_columns.docx")
```

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A footnote is a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting a footnote adds a small superscript reference symbol
# at the main body text where we insert the footnote.
# Each footnote also creates an entry at the bottom of the page, consisting of a symbol
# that matches the reference symbol in the main body text.
# The reference text that we pass to the document builder's "insert_footnote" method.
builder.write("Hello world!")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote contents.")

# We can use the "position" property to determine where the document will place all its footnotes.
# If we set the value of the "position" property to "FootnotePosition.BOTTOM_OF_PAGE",
# every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
# If we set the value of the "position" property to "FootnotePosition.BENEATH_TEXT",
# every footnote will show up at the end of the page's text that contains its reference mark.
doc.footnote_options.position = footnote_position

doc.save(ARTIFACTS_DIR + "InlineStory.position_footnote.docx")
```

Shows how to change the number style of footnote/endnote reference marks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Footnotes and endnotes are a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting a footnote/endnote adds a small superscript reference symbol
# at the main body text where we insert the footnote/endnote.
# Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
# symbol in the main body text. The reference text that we pass to the document builder's "insert_endnote" method.
# Footnote entries, by default, show up at the bottom of each page that contains
# their reference symbols, and endnotes show up at the end of the document.
builder.write("Text 1. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 1.")
builder.write("Text 2. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 2.")
builder.write("Text 3. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark")

builder.insert_paragraph()

builder.write("Text 1. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 1.")
builder.write("Text 2. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 2.")
builder.write("Text 3. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark")

# By default, the reference symbol for each footnote and endnote is its index
# among all the document's footnotes/endnotes. Each document maintains separate counts
# for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
# and endnotes display their numbers in lowercase Roman numerals.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)

# We can use the "number_style" property to apply custom numbering styles to footnotes and endnotes.
# This will not affect footnotes/endnotes with custom reference marks.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER

doc.save(ARTIFACTS_DIR + "InlineStory.ref_mark_number_style.docx")
```

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Footnotes and endnotes are a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting a footnote/endnote adds a small superscript reference symbol
# at the main body text where we insert the footnote/endnote.
# Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
# symbol in the main body text. The reference text that we pass to the document builder's "insert_endnote" method.
# Footnote entries, by default, show up at the bottom of each page that contains
# their reference symbols, and endnotes show up at the end of the document.
builder.write("Text 1. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 1.")
builder.write("Text 2. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write("Text 3. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 3.")
builder.write("Text 4. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 4.")

builder.insert_break(aw.BreakType.PAGE_BREAK)

builder.write("Text 1. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 1.")
builder.write("Text 2. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 2.")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write("Text 3. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 3.")
builder.write("Text 4. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 4.")

# By default, the reference symbol for each footnote and endnote is its index
# among all the document's footnotes/endnotes. Each document maintains separate counts
# for footnotes and endnotes and does not restart these counts at any point.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)

# We can use the "restart_rule" property to get the document to restart
# the footnote/endnote counts at a new page or section.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION

doc.save(ARTIFACTS_DIR + "InlineStory.numbering_rule.docx")
```

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Footnotes and endnotes are a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting a footnote/endnote adds a small superscript reference symbol
# at the main body text where we insert the footnote/endnote.
# Each footnote/endnote also creates an entry, which consists of a symbol
# that matches the reference symbol in the main body text.
# The reference text that we pass to the document builder's "insert_endnote" method.
# Footnote entries, by default, show up at the bottom of each page that contains
# their reference symbols, and endnotes show up at the end of the document.
builder.write("Text 1. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 1.")
builder.write("Text 2. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 2.")
builder.write("Text 3. ")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "Footnote 3.")

builder.insert_paragraph()

builder.write("Text 1. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 1.")
builder.write("Text 2. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 2.")
builder.write("Text 3. ")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote 3.")

# By default, the reference symbol for each footnote and endnote is its index
# among all the document's footnotes/endnotes. Each document maintains separate counts
# for footnotes and for endnotes, which both begin at 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)

# We can use the "start_number" property to get the document to
# begin a footnote or endnote count at a different number.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50

doc.save(ARTIFACTS_DIR + "InlineStory.start_number.docx")
```

### See Also

* module [aspose.words.notes](../)
* property [Document.footnote_options](../../aspose.words/document/footnote_options/)
* property [PageSetup.footnote_options](../../aspose.words/pagesetup/footnote_options/)

