---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# An endnote is a way to attach a reference or a side comment to text
# that does not interfere with the main body text's flow.
# Inserting an endnote adds a small superscript reference symbol
# at the main body text where we insert the endnote.
# Each endnote also creates an entry at the end of the document, consisting of a symbol
# that matches the reference symbol in the main body text.
# The reference text that we pass to the document builder's "insert_endnote" method.
builder.write("Hello world!")
builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, "Endnote contents.")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write("This is the second section.")

# We can use the "position" property to determine where the document will place all its endnotes.
# If we set the value of the "position" property to "EndnotePosition.END_OF_DOCUMENT",
# every footnote will show up in a collection at the end of the document. This is the default value.
# If we set the value of the "position" property to "EndnotePosition.END_OF_SECTION",
# every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
doc.endnote_options.position = endnote_position

doc.save(ARTIFACTS_DIR + "InlineStory.position_endnote.docx")
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

