---
title: CellCollection indexer
linktitle: CellCollection indexer
articleTitle: CellCollection indexer
second_title: Aspose.Words for Python
description: "CellCollection indexer. Retrieves a [Cell](../../cell/) at the given index."
type: docs
weight: 10
url: /python-net/aspose.words.tables/cellcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Cell](../../cell/) at the given index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
tables = doc.first_section.body.tables
self.assertEqual(2, len(list(tables)))
i = 0
while i < tables.count:
    print(f'Start of Table {i}')
    rows = tables[i].rows
    # We can use the "ToArray" method on a row collection to clone it into an array.
    self.assertSequenceEqual(list(rows), list(rows))
    self.assertNotEqual(rows, list(rows))
    j = 0
    while j < rows.count:
        print(f'\tStart of Row {j}')
        cells = rows[j].cells
        # We can use the "ToArray" method on a cell collection to clone it into an array.
        self.assertSequenceEqual(list(cells), list(cells))
        self.assertNotEqual(cells, list(cells))
        k = 0
        while k < cells.count:
            cell_text = cells[k].to_string(save_format=aw.SaveFormat.TEXT).strip()
            print(f'\t\tContents of Cell:{k} = "{cell_text}"')
            k += 1
        print(f'\tEnd of Row {j}')
        j += 1
    print(f'End of Table {i}\n')
    i += 1
```

### See Also

* module [aspose.words.tables](../../)
* class [CellCollection](../)

