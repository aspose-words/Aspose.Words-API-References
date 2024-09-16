---
title: TableStyle.left_indent property
linktitle: left_indent property
articleTitle: left_indent property
second_title: Aspose.Words for Python
description: "TableStyle.left_indent property. Gets or sets the value that represents the left indent of a table."
type: docs
weight: 90
url: /python-net/aspose.words/tablestyle/left_indent/
---

## TableStyle.left_indent property

Gets or sets the value that represents the left indent of a table.


```python
@property
def left_indent(self) -> float:
    ...

@left_indent.setter
def left_indent(self, value: float):
    ...

```

### Examples

Shows how to set the position of a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Below are two ways of aligning a table horizontally.
# 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.alignment = aw.tables.TableAlignment.CENTER
table_style.borders.color = aspose.pydrawing.Color.blue
table_style.borders.line_style = aw.LineStyle.SINGLE
# Insert a table and apply the style we created to it.
table = builder.start_table()
builder.insert_cell()
builder.write('Aligned to the center of the page')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
table.style = table_style
# 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle2').as_table_style()
table_style.left_indent = 55
table_style.borders.color = aspose.pydrawing.Color.green
table_style.borders.line_style = aw.LineStyle.SINGLE
table = builder.start_table()
builder.insert_cell()
builder.write('Aligned according to left indent')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
table.style = table_style
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetTableAlignment.docx')
```

### See Also

* module [aspose.words](../../)
* class [TableStyle](../)

