---
title: CellCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Retrieves a Cell at the given index."
type: docs
weight: 10
url: /python-net/aspose.words.tables/cellcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a **Cell** at the given index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
tables = doc.first_section.body.tables

self.assertEqual(2, len(tables.to_array()))

for i in range(tables.count):
    print(f"Start of Table {i}")

    rows = tables[i].rows

    # We can use the "to_array" method on a row collection to clone it into an array.
    self.assertSequenceEqual(list(rows), rows.to_array())
    #Assert.are_not_same(rows, rows.to_array())

    for j in range(rows.count):
        print(f"\tStart of Row {j}")

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

### See Also

* module [aspose.words.tables](../../)
* class [CellCollection](../)

