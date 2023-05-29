---
title: Table.rows property
linktitle: rows property
articleTitle: rows property
second_title: Aspose.Words for Python
description: "Table.rows property. Provides typed access to the rows of the table."
type: docs
weight: 260
url: /python-net/aspose.words.tables/table/rows/
---

## Table.rows property

Provides typed access to the rows of the table.


### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
tables = doc.first_section.body.tables

self.assertEqual(2, len(tables.to_array()))

for i in range(tables.count):
    print("Start of Table", i)

    rows = tables[i].rows

    # We can use the "to_array" method on a row collection to clone it into an array.
    self.assertSequenceEqual(list(rows), rows.to_array())
    #Assert.are_not_same(rows, rows.to_array())

    for j in range(rows.count):
        print("\tStart of Row", j)

        cells = rows[j].cells

        # We can use the "to_array" method on a cell collection to clone it into an array.
        self.assertSequenceEqual(list(cells), cells.to_array())
        #Assert.are_not_same(cells, cells.to_array())

        for k in range(cells.count):
            cell_text = cells[k].to_string(aw.SaveFormat.TEXT).strip()
            print(f"\t\tContents of Cell:{k} = \"{cell_text}\"")

        print(f"\tEnd of Row {j}")

    print(f"End of Table {i}\n")
```

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
* class [Table](../)

