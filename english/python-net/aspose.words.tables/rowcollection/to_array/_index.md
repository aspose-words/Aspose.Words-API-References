---
title: to_array method
second_title: Aspose.Words for Python via .NET API Reference
description: "Copies all rows from the collection to a new array of rows."
type: docs
weight: 20
url: /python-net/aspose.words.tables/rowcollection/to_array/
---

## to_array() {#default}

Copies all rows from the collection to a new array of rows.


```python
def to_array(self):
    ...
```

### Returns

An array of rows.


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
* class [RowCollection](../)

