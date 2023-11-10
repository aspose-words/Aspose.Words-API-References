---
title: CellFormat.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "CellFormat.borders property. Gets collection of borders of the cell."
type: docs
weight: 10
url: /python-net/aspose.words.tables/cellformat/borders/
---

## CellFormat.borders property

Gets collection of borders of the cell.


```python
@property
def borders(self) -> aspose.words.BorderCollection:
    ...

```

### Examples

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

# Below are two ways of getting a table from a document.
# 1 -  From the "tables" collection of a Body node:
first_table = doc.first_section.body.tables[0]

# 2 -  Using the "get_child" method:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()

# Append all rows from the current table to the next.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)

# Remove the empty table container.
second_table.remove()

doc.save(ARTIFACTS_DIR + "Table.combine_tables.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

