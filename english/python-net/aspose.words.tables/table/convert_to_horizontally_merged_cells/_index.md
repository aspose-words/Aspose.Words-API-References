---
title: Table.convert_to_horizontally_merged_cells method
linktitle: convert_to_horizontally_merged_cells method
articleTitle: convert_to_horizontally_merged_cells method
second_title: Aspose.Words for Python
description: "Table.convert_to_horizontally_merged_cells method. Converts cells horizontally merged by width to cells merged by [CellFormat.horizontal_merge](../../cellformat/horizontal_merge/)."
type: docs
weight: 410
url: /python-net/aspose.words.tables/table/convert_to_horizontally_merged_cells/
---

## convert_to_horizontally_merged_cells() {#default}

Converts cells horizontally merged by width to cells merged by [CellFormat.horizontal_merge](../../cellformat/horizontal_merge/).



```python
def convert_to_horizontally_merged_cells(self):
    ...
```

### Remarks

Table cells can be horizontally merged either using merge flags [CellFormat.horizontal_merge](../../cellformat/horizontal_merge/) or using cell width [CellFormat.width](../../cellformat/width/).

When table cell is merged by width property [CellFormat.horizontal_merge](../../cellformat/horizontal_merge/) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.




### Examples

Shows how to convert cells horizontally merged by width to cells merged by CellFormat.horizontal_merge.

```python
doc = aw.Document(MY_DIR + 'Table with merged cells.docx')
# Microsoft Word does not write merge flags anymore, defining merged cells by width instead.
# Aspose.Words by default define only 5 cells in a row, and none of them have the horizontal merge flag,
# even though there were 7 cells in the row before the horizontal merging took place.
table = doc.first_section.body.tables[0]
row = table.rows[0]
self.assertEqual(5, row.cells.count)
self.assertTrue(all((c.as_cell().cell_format.horizontal_merge == aw.tables.CellMerge.NONE for c in row.cells)))
# Use the "convert_to_horizontally_merged_cells" method to convert cells horizontally merged
# by its width to the cell horizontally merged by flags.
# Now, we have 7 cells, and some of them have horizontal merge values.
table.convert_to_horizontally_merged_cells()
row = table.rows[0]
self.assertEqual(7, row.cells.count)
self.assertEqual(aw.tables.CellMerge.NONE, row.cells[0].cell_format.horizontal_merge)
self.assertEqual(aw.tables.CellMerge.FIRST, row.cells[1].cell_format.horizontal_merge)
self.assertEqual(aw.tables.CellMerge.PREVIOUS, row.cells[2].cell_format.horizontal_merge)
self.assertEqual(aw.tables.CellMerge.NONE, row.cells[3].cell_format.horizontal_merge)
self.assertEqual(aw.tables.CellMerge.FIRST, row.cells[4].cell_format.horizontal_merge)
self.assertEqual(aw.tables.CellMerge.PREVIOUS, row.cells[5].cell_format.horizontal_merge)
self.assertEqual(aw.tables.CellMerge.NONE, row.cells[6].cell_format.horizontal_merge)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

