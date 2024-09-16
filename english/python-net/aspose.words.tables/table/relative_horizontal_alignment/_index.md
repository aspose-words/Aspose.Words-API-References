---
title: Table.relative_horizontal_alignment property
linktitle: relative_horizontal_alignment property
articleTitle: relative_horizontal_alignment property
second_title: Aspose.Words for Python
description: "Table.relative_horizontal_alignment property. Gets or sets floating table relative horizontal alignment."
type: docs
weight: 230
url: /python-net/aspose.words.tables/table/relative_horizontal_alignment/
---

## Table.relative_horizontal_alignment property

Gets or sets floating table relative horizontal alignment.


```python
@property
def relative_horizontal_alignment(self) -> aspose.words.drawing.HorizontalAlignment:
    ...

@relative_horizontal_alignment.setter
def relative_horizontal_alignment(self, value: aspose.words.drawing.HorizontalAlignment):
    ...

```

### Examples

Shows how set the location of floating tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Table 1, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Set the table's location to a place on the page, such as, in this case, the bottom right corner.
table.relative_vertical_alignment = aw.drawing.VerticalAlignment.BOTTOM
table.relative_horizontal_alignment = aw.drawing.HorizontalAlignment.RIGHT
table = builder.start_table()
builder.insert_cell()
builder.write('Table 2, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
table.absolute_vertical_distance = 50
table.absolute_horizontal_distance = 100
doc.save(file_name=ARTIFACTS_DIR + 'Table.ChangeFloatingTableProperties.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

