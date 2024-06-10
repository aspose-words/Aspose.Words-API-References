---
title: TableStyle.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "TableStyle.alignment property. Specifies the alignment for the table style."
type: docs
weight: 10
url: /python-net/aspose.words/tablestyle/alignment/
---

## TableStyle.alignment property

Specifies the alignment for the table style.


```python
@property
def alignment(self) -> aspose.words.tables.TableAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.tables.TableAlignment):
    ...

```

### Remarks

The default value is [TableAlignment.LEFT](../../../aspose.words.tables/tablealignment/#LEFT).



### Examples

Shows how to set the position of a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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

