---
title: Table.top_padding property
linktitle: top_padding property
articleTitle: top_padding property
second_title: Aspose.Words for Python
description: "Table.top_padding property. Gets or sets the amount of space (in points) to add above the contents of cells."
type: docs
weight: 330
url: /tr/python-net/aspose.words.tables/table/top_padding/
---

## Table.top_padding property

Gets or sets the amount of space (in points) to add above the contents of cells.


```python
@property
def top_padding(self) -> float:
    ...

@top_padding.setter
def top_padding(self, value: float):
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

