---
title: TextColumnCollection.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "TextColumnCollection.width property. When columns are evenly spaced, gets the width of the columns."
type: docs
weight: 60
url: /python-net/aspose.words/textcolumncollection/width/
---

## TextColumnCollection.width property

When columns are evenly spaced, gets the width of the columns.


```python
@property
def width(self) -> float:
    ...

```

### Remarks

Has effect only when [TextColumnCollection.evenly_spaced](../evenly_spaced/) is set to ``True``.




### Examples

Shows how to create multiple evenly spaced columns in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
columns = builder.page_setup.text_columns
columns.spacing = 100
columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ColumnsSameWidth.docx')
```

### See Also

* module [aspose.words](../../)
* class [TextColumnCollection](../)

