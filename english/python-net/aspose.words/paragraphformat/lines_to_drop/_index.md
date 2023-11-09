---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /python-net/aspose.words/paragraphformat/lines_to_drop/
---

## ParagraphFormat.lines_to_drop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```python
@property
def lines_to_drop(self) -> int:
    ...

@lines_to_drop.setter
def lines_to_drop(self, value: int):
    ...

```

### Examples

Shows how to set the size of a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Modify the "lines_to_drop" property to designate a paragraph as a drop cap,
# which will turn it into a large capital letter that will decorate the next paragraph.
# Give this property a value of 4 to give the drop cap the height of four text lines.
builder.paragraph_format.lines_to_drop = 4
builder.writeln("H")

# Reset the "lines_to_drop" property to 0 to turn the next paragraph into an ordinary paragraph.
# The text in this paragraph will wrap around the drop cap.
builder.paragraph_format.lines_to_drop = 0
builder.writeln("ello world!")

doc.save(ARTIFACTS_DIR + "ParagraphFormat.lines_to_drop.odt")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

