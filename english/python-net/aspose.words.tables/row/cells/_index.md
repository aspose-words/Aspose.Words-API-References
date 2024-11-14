---
title: Row.cells property
linktitle: cells property
articleTitle: cells property
second_title: Aspose.Words for Python
description: "Row.cells property. Provides typed access to the [Cell](../../cell/) child nodes of the row."
type: docs
weight: 20
url: /python-net/aspose.words.tables/row/cells/
---

## Row.cells property

Provides typed access to the [Cell](../../cell/) child nodes of the row.



```python
@property
def cells(self) -> aspose.words.tables.CellCollection:
    ...

```

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
* class [Row](../)

