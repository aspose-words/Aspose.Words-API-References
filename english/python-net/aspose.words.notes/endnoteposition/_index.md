﻿---
title: EndnotePosition enumeration
linktitle: EndnotePosition enumeration
articleTitle: EndnotePosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.EndnotePosition enumeration. Defines the endnote position."
type: docs
weight: 20
url: /python-net/aspose.words.notes/endnoteposition/
---

## EndnotePosition enumeration

Defines the endnote position.


### Members

| Name | Description |
| --- | --- |
| END_OF_SECTION | Endnotes are output at the end of the section. |
| END_OF_DOCUMENT | Endnotes are output at the end of the document. |

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# An endnote is a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting an endnote adds a small superscript reference symbol
# at the main body text where we insert the endnote.
# Each endnote also creates an entry at the end of the document, consisting of a symbol
# that matches the reference symbol in the main body text.
# The reference text that we pass to the document builder's "InsertEndnote" method.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# We can use the "Position" property to determine where the document will place all its endnotes.
# If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
# every footnote will show up in a collection at the end of the document. This is the default value.
# If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
# every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [EndnoteOptions](../endnoteoptions/)

