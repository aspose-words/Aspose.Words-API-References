---
title: Table.convert_to_horizontally_merged_cells method
linktitle: convert_to_horizontally_merged_cells method
articleTitle: convert_to_horizontally_merged_cells method
second_title: Aspose.Words for Python
description: "Table.convert_to_horizontally_merged_cells method. Converts cells horizontally merged by width to cells merged by [CellFormat.horizontal_merge](../../cellformat/horizontal_merge/)."
type: docs
weight: 410
url: /sv/python-net/aspose.words.tables/table/convert_to_horizontally_merged_cells/
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
# Microsoft Word skriver inte längre sammanslagningsflaggor, utan definierar sammanslagna celler efter bredd istället.
# Aspose.Words definierar som standard bara 5 celler i en rad, och ingen av dem har den horisontella sammanslagningsflaggan,
# även om det fanns 7 celler i raden innan den horisontella sammanslagningen ägde rum.
table = doc.first_section.body.tables[0]
row = table.rows[0]
self.assertEqual(5, row.cells.count)
self.assertTrue(all([c.as_cell().cell_format.horizontal_merge == aw.tables.CellMerge.NONE for c in row.cells]))
# Använd metoden "ConvertToHorizontallyMergedCells" för att konvertera celler som är horisontellt sammanslagna
# efter dess bredd till cellen som är horisontellt sammanslagen med flaggor.
# Nu har vi 7 celler, och några av dem har horisontella sammanslagningsvärden.
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

