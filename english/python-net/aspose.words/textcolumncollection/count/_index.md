---
title: TextColumnCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "TextColumnCollection.count property. Gets the number of columns in the section of a document."
type: docs
weight: 20
url: /python-net/aspose.words/textcolumncollection/count/
---

## TextColumnCollection.count property

Gets the number of columns in the section of a document.


```python
@property
def count(self) -> int:
    ...

```

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

