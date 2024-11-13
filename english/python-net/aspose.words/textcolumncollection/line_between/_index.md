---
title: TextColumnCollection.line_between property
linktitle: line_between property
articleTitle: line_between property
second_title: Aspose.Words for Python
description: "TextColumnCollection.line_between property. When ``True``, adds a vertical line between columns."
type: docs
weight: 40
url: /python-net/aspose.words/textcolumncollection/line_between/
---

## TextColumnCollection.line_between property

When ``True``, adds a vertical line between columns.



```python
@property
def line_between(self) -> bool:
    ...

@line_between.setter
def line_between(self, value: bool):
    ...

```

### Examples

Shows how to separate columns with a vertical line.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Configure the current section's PageSetup object to divide the text into several columns.
# Set the "LineBetween" property to "true" to put a dividing line between columns.
# Set the "LineBetween" property to "false" to leave the space between columns blank.
columns = builder.page_setup.text_columns
columns.line_between = line_between
columns.set_count(3)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 3.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.VerticalLineBetweenColumns.docx')
```

### See Also

* module [aspose.words](../../)
* class [TextColumnCollection](../)

