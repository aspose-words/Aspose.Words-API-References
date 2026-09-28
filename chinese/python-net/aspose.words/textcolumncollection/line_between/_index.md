---
title: TextColumnCollection.line_between property
linktitle: line_between property
articleTitle: line_between property
second_title: Aspose.Words for Python
description: "TextColumnCollection.line_between property. When ``True``, adds a vertical line between columns."
type: docs
weight: 40
url: /zh/python-net/aspose.words/textcolumncollection/line_between/
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
# 配置当前章节的 PageSetup 对象，将文本分成多列。
# 将 "LineBetween" 属性设为 "true"，以在列之间放置分隔线。
# 将 "LineBetween" 属性设为 "false"，以保持列间空白。
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

