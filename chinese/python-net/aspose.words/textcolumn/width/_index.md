---
title: TextColumn.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "TextColumn.width property. Gets or sets the width of the text column in points."
type: docs
weight: 20
url: /zh/python-net/aspose.words/textcolumn/width/
---

## TextColumn.width property

Gets or sets the width of the text column in points.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
    ...

```

### Examples

Shows how to create unevenly spaced columns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
page_setup = builder.page_setup
columns = page_setup.text_columns
columns.evenly_spaced = False
columns.set_count(2)
# 确定我们可用于排列列的空间量。
content_width = page_setup.page_width - page_setup.left_margin - page_setup.right_margin
self.assertAlmostEqual(470.3, content_width, delta=0.01)
# 将第一列设置为窄列。
column = columns[0]
column.width = 100
column.space_after = 20
# 将第二列设置为占据页面边距内剩余的可用空间。
column = columns[1]
column.width = content_width - column.width - column.space_after
builder.writeln('Narrow column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Wide column 2.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.CustomColumnWidth.docx')
```

### See Also

* module [aspose.words](../../)
* class [TextColumn](../)

