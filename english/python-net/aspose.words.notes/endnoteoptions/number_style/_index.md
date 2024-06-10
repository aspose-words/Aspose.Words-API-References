---
title: EndnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "EndnoteOptions.number_style property. Specifies the number format for automatically numbered endnotes."
type: docs
weight: 10
url: /python-net/aspose.words.notes/endnoteoptions/number_style/
---

## EndnoteOptions.number_style property

Specifies the number format for automatically numbered endnotes.


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
builder = aw.DocumentBuilder(doc)
# Footnotes and endnotes are a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting a footnote/endnote adds a small superscript reference symbol
# at the main body text where we insert the footnote/endnote.
# Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
# symbol in the main body text. The reference text that we pass to the document builder's "insert_endnote" method.
# Footnote entries, by default, show up at the bottom of each page that contains
# their reference symbols, and endnotes show up at the end of the document.
builder.write('Text 1. ')
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote 3.', 'Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, 'Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, 'Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, 'Endnote 3.', 'Custom endnote reference mark')
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
doc.save(ARTIFACTS_DIR + 'InlineStory.ref_mark_number_style.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

