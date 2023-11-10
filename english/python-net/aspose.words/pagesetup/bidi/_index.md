---
title: PageSetup.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "PageSetup.bidi property. Specifies that this section contains bidirectional (complex scripts) text."
type: docs
weight: 10
url: /python-net/aspose.words/pagesetup/bidi/
---

## PageSetup.bidi property

Specifies that this section contains bidirectional (complex scripts) text.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the columns in this section are laid out from right to left.




### Examples

Shows how to set the order of text columns in a section.

```python
doc = aw.Document()

page_setup = doc.sections[0].page_setup
page_setup.text_columns.set_count(3)

builder = aw.DocumentBuilder(doc)
builder.write("Column 1.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.write("Column 2.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.write("Column 3.")

# Set the "bidi" property to "True" to arrange the columns starting from the page's right side.
# The order of the columns will match the direction of the right-to-left text.
# Set the "bidi" property to "False" to arrange the columns starting from the page's left side.
# The order of the columns will match the direction of the left-to-right text.
page_setup.bidi = reverse_columns

doc.save(ARTIFACTS_DIR + "PageSetup.bidi.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

