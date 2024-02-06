---
title: Footnote.footnote_type property
linktitle: footnote_type property
articleTitle: footnote_type property
second_title: Aspose.Words for Python
description: "Footnote.footnote_type property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /python-net/aspose.words.notes/footnote/footnote_type/
---

## Footnote.footnote_type property

Returns a value that specifies whether this is a footnote or endnote.


```python
@property
def footnote_type(self) -> aspose.words.notes.FootnoteType:
    ...

```

### Examples

Shows the difference between footnotes and endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two ways of attaching numbered references to the text. Both these references will add a
# small superscript reference mark at the location that we insert them.
# The reference mark, by default, is the index number of the reference among all the references in the document.
# Each reference will also create an entry, which will have the same reference mark as in the body text
# and reference text, which we will pass to the document builder's "insert_footnote" method.
# 1 -  A footnote, whose entry will appear on the same page as the text that it references:
builder.write("Footnote referenced main body text.")
footnote = builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE,
    "Footnote text, will appear at the bottom of the page that contains the referenced text.")

# 2 -  An endnote, whose entry will appear at the end of the document:
builder.write("Endnote referenced main body text.")
endnote = builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE,
    "Endnote text, will appear at the very end of the document.")

builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)

self.assertEqual(aw.notes.FootnoteType.FOOTNOTE, footnote.footnote_type)
self.assertEqual(aw.notes.FootnoteType.ENDNOTE, endnote.footnote_type)

doc.save(ARTIFACTS_DIR + "InlineStory.footnote_endnote.docx")
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

