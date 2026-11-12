---
title: Table.left_padding property
linktitle: left_padding property
articleTitle: left_padding property
second_title: Aspose.Words for Python
description: "Table.left_padding property. Gets or sets the amount of space (in points) to add to the left of the contents of cells."
type: docs
weight: 200
url: /tr/python-net/aspose.words.tables/table/left_padding/
---

## Table.left_padding property

Gets or sets the amount of space (in points) to add to the left of the contents of cells.


```python
@property
def left_padding(self) -> float:
    ...

@left_padding.setter
def left_padding(self, value: float):
    ...

```

### Examples

Shows how to configure content padding in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_table()
# Tablodaki her hücre için, içeriği ile kenarları arasındaki mesafeyi ayarlayın.
# Bu tablo, metni kaydırarak minimum dolgu mesafesini koruyacaktır.
table.left_padding = 30
table.right_padding = 60
table.top_padding = 10
table.bottom_padding = 90
table.preferred_width = aw.tables.PreferredWidth.from_points(250)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

