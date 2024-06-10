---
title: FootnoteType enumeration
linktitle: FootnoteType enumeration
articleTitle: FootnoteType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteType enumeration. Specifies whether this is a footnote or an endnote."
type: docs
weight: 70
url: /python-net/aspose.words.notes/footnotetype/
---

## FootnoteType enumeration

Specifies whether this is a footnote or an endnote.

Both footnotes and endnotes are represented by objects by the [FootnoteType.FOOTNOTE](./#FOOTNOTE)
class. Use [Footnote.footnote_type](../footnote/footnote_type/) to distinguish between footnotes 
and endnotes.




### Members

| Name | Description |
| --- | --- |
| FOOTNOTE | The object is a footnote. |
| ENDNOTE | The object is an endnote. |

### Examples

Shows how to reference text with a footnote and an endnote.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert some text and mark it with a footnote with the "is_auto" property set to "True" by default,
# so the marker seen in the body text will be auto-numbered at "1",
# and the footnote will appear at the bottom of the page.
builder.write('This text will be referenced by a footnote.')
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote comment regarding referenced text.')
# Insert more text and mark it with an endnote with a custom reference mark,
# which will be used in place of the number "2" and set "is_auto" to False.
builder.write('This text will be referenced by an endnote.')
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, 'Endnote comment regarding referenced text.', 'CustomMark')
# Footnotes always appear at the bottom of their referenced text,
# so this page break will not affect the footnote.
# On the other hand, endnotes are always at the end of the document
# so that this page break will push the endnote down to the next page.
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc.save(ARTIFACTS_DIR + 'DocumentBuilder.insert_footnote.docx')
```

Shows how to insert and customize footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Add text, and reference it with a footnote. This footnote will place a small superscript reference
# mark after the text that it references and create an entry below the main body text at the bottom of the page.
# This entry will contain the footnote's reference mark and the reference text,
# which we will pass to the document builder's "insert_footnote" method.
builder.write('Main body text.')
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote text.')
# If this property is set to "True", then our footnote's reference mark
# will be its index among all the section's footnotes.
# This is the first footnote, so the reference mark will be "1".
self.assertTrue(footnote.is_auto)
# We can move the document builder inside the footnote to edit its reference text.
builder.move_to(footnote.first_paragraph)
builder.write(' More text added by a DocumentBuilder.')
builder.move_to_document_end()
self.assertEqual('\x02 Footnote text. More text added by a DocumentBuilder.', footnote.get_text().strip())
builder.write(' More main body text.')
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote text.')
# We can set a custom reference mark which the footnote will use instead of its index number.
footnote.reference_mark = 'RefMark'
self.assertFalse(footnote.is_auto)
# A bookmark with the "is_auto" flag set to True will still show its real index
# even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.write(' More main body text.')
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, 'Footnote text.')
self.assertTrue(footnote.is_auto)
doc.save(ARTIFACTS_DIR + 'InlineStory.add_footnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* enum value [FootnoteType.FOOTNOTE](./#FOOTNOTE)

