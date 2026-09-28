---
title: Table.convert_to_horizontally_merged_cells method
linktitle: convert_to_horizontally_merged_cells method
articleTitle: convert_to_horizontally_merged_cells method
second_title: Aspose.Words for Python
description: "Table.convert_to_horizontally_merged_cells method. Converts cells horizontally merged by width to cells merged by [CellFormat.horizontal_merge](../../cellformat/horizontal_merge/)."
type: docs
weight: 410
url: /de/python-net/aspose.words.tables/table/convert_to_horizontally_merged_cells/
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

Shows how to convert cells horizontally merged by width to cells merged by CellFormat.HorizontalMerge.

```python
doc = aw.Document(file_name=MY_DIR + 'Table with merged cells.docx')
# Microsoft Word schreibt keine Zusammenführungs‑Flags mehr, sondern definiert zusammengeführte Zellen anhand ihrer Breite.
# Aspose.Words definiert standardmäßig nur 5 Zellen in einer Zeile, und keine von ihnen hat das horizontale Zusammenführungs‑Flag,
# obwohl es vor dem horizontalen Zusammenführen 7 Zellen in der Zeile gab.
table = doc.first_section.body.tables[0]
row = table.rows[0]
self.assertEqual(5, row.cells.count)
self.assertTrue(all([c.as_cell().cell_format.horizontal_merge == aw.tables.CellMerge.NONE for c in row.cells]))
# Verwenden Sie die Methode "ConvertToHorizontallyMergedCells", um Zellen, die horizontal zusammengeführt wurden,
# nach ihrer Breite in die Zelle, die durch Flags horizontal zusammengeführt wurde.
# Jetzt haben wir 7 Zellen, und einige von ihnen haben horizontale Zusammenführungswerte.
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

