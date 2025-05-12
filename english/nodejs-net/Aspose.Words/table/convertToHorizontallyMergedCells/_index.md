---
title: Table.convertToHorizontallyMergedCells method
linktitle: convertToHorizontallyMergedCells method
articleTitle: convertToHorizontallyMergedCells method
second_title: Aspose.Words for Node.js
description: "Table.convertToHorizontallyMergedCells method. Converts cells horizontally merged by width to cells merged by [CellFormat.horizontalMerge](../../../aspose.words.tables/cellformat/horizontalMerge/)."
type: docs
weight: 380
url: /nodejs-net/aspose.words/table/convertToHorizontallyMergedCells/
---

## convertToHorizontallyMergedCells() {#default}

Converts cells horizontally merged by width to cells merged by [CellFormat.horizontalMerge](../../../aspose.words.tables/cellformat/horizontalMerge/).



```js
convertToHorizontallyMergedCells()
```

### Remarks

Table cells can be horizontally merged either using merge flags [CellFormat.horizontalMerge](../../../aspose.words.tables/cellformat/horizontalMerge/) or using cell width [CellFormat.width](../../../aspose.words.tables/cellformat/width/).

When table cell is merged by width property [CellFormat.horizontalMerge](../../../aspose.words.tables/cellformat/horizontalMerge/) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.




### Examples

Shows how to convert cells horizontally merged by width to cells merged by CellFormat.horizontalMerge.

```js
let doc = new aw.Document(base.myDir + "Table with merged cells.docx");

// Microsoft Word does not write merge flags anymore, defining merged cells by width instead.
// Aspose.words by default define only 5 cells in a row, and none of them have the horizontal merge flag,
// even though there were 7 cells in the row before the horizontal merging took place.
let table = doc.firstSection.body.tables.at(0);
let row = table.rows.at(0);

expect(row.cells.count).toEqual(5);
expect(row.cells.toArray().every(c => c.cellFormat.horizontalMerge == aw.Tables.CellMerge.None)).toEqual(true);

// Use the "ConvertToHorizontallyMergedCells" method to convert cells horizontally merged
// by its width to the cell horizontally merged by flags.
// Now, we have 7 cells, and some of them have horizontal merge values.
table.convertToHorizontallyMergedCells();
row = table.rows.at(0);

expect(row.cells.count).toEqual(7);

expect(row.cells.at(0).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.None);
expect(row.cells.at(1).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.First);
expect(row.cells.at(2).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.Previous);
expect(row.cells.at(3).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.None);
expect(row.cells.at(4).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.First);
expect(row.cells.at(5).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.Previous);
expect(row.cells.at(6).cellFormat.horizontalMerge).toEqual(aw.Tables.CellMerge.None);
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

