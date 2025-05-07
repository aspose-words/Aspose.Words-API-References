---
title: CellFormat.verticalMerge property
linktitle: verticalMerge property
articleTitle: verticalMerge property
second_title: Aspose.Words for Node.js
description: "CellFormat.verticalMerge property. Specifies how the cell is merged with other cells vertically."
type: docs
weight: 130
url: /nodejs-net/aspose.words.tables/cellformat/verticalMerge/
---

## CellFormat.verticalMerge property

Specifies how the cell is merged with other cells vertically.


```js
get verticalMerge(): Aspose.Words.Tables.CellMerge
```

### Remarks

Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated.
The consolidated area is used to display the contents of the first vertically merged cell
and all other vertically merged cells must be empty.




### Examples

Prints the horizontal and vertical merge type of a cell.

```js
test('CheckCellsMerged', () => {
  let doc = new aw.Document(base.myDir + "Table with merged cells.docx");
  let table = doc.firstSection.body.tables.at(0);

  for (let row of table.rows.toArray())
    for (let cell of row.cells.toArray())
      console.log(printCellMergeType(cell));
  expect(printCellMergeType(table.firstRow.firstCell)).toEqual("The cell at R1, C1 is vertically merged");
});


function printCellMergeType(cell)
{
  let isHorizontallyMerged = cell.cellFormat.horizontalMerge != aw.Tables.CellMerge.None;
  let isVerticallyMerged = cell.cellFormat.verticalMerge != aw.Tables.CellMerge.None;
  let cellLocation =
    `R${cell.parentRow.parentTable.indexOf(cell.parentRow) + 1}, C${cell.parentRow.indexOf(cell) + 1}`;

  if (isHorizontallyMerged && isVerticallyMerged)
    return `The cell at ${cellLocation} is both horizontally and vertically merged`;
  if (isHorizontallyMerged)
    return `The cell at ${cellLocation} is horizontally merged.`;

  return isVerticallyMerged ? `The cell at ${cellLocation} is vertically merged` : `The cell at ${cellLocation} is not merged`;
}
```

Shows how to merge table cells vertically.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of vertically merged cells.
builder.insertCell();
builder.cellFormat.verticalMerge = aw.Tables.CellMerge.First;
builder.write("Text in merged cells.");

// Insert a cell into the second column of the first row, then end the row.
// Also, configure the builder to disable vertical merging in created cells.
builder.insertCell();
builder.cellFormat.verticalMerge = aw.Tables.CellMerge.None;
builder.write("Text in unmerged cell.");
builder.endRow();

// Insert a cell into the first column of the second row. 
// Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
builder.insertCell();
builder.cellFormat.verticalMerge = aw.Tables.CellMerge.Previous;

// Insert another independent cell in the second column of the second row.
builder.insertCell();
builder.cellFormat.verticalMerge = aw.Tables.CellMerge.None;
builder.write("Text in unmerged cell.");
builder.endRow();
builder.endTable();

doc.save(base.artifactsDir + "CellFormat.verticalMerge.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [CellFormat](../)
* property [CellFormat.horizontalMerge](../horizontalMerge/)

