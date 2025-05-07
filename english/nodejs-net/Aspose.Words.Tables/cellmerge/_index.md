---
title: CellMerge enumeration
linktitle: CellMerge enumeration
articleTitle: CellMerge enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Tables.CellMerge enumeration. Specifies how a cell in a table is merged with other cells."
type: docs
weight: 50
url: /nodejs-net/aspose.words.tables/cellmerge/
---

## CellMerge enumeration

Specifies how a cell in a table is merged with other cells.


### Members

| Name | Description |
| --- | --- |
| None | The cell is not merged. |
| First | The cell is the first cell in a range of merged cells. |
| Previous | The cell is merged to the previous cell horizontally or vertically. |

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

Shows how to merge table cells horizontally.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a cell into the first column of the first row.
// This cell will be the first in a range of horizontally merged cells.
builder.insertCell();
builder.cellFormat.horizontalMerge = aw.Tables.CellMerge.First;
builder.write("Text in merged cells.");

// Insert a cell into the second column of the first row. Instead of adding text contents,
// we will merge this cell with the first cell that we added directly to the left.
builder.insertCell();
builder.cellFormat.horizontalMerge = aw.Tables.CellMerge.Previous;
builder.endRow();

// Insert two more unmerged cells to the second row.
builder.cellFormat.horizontalMerge = aw.Tables.CellMerge.None;
builder.insertCell();
builder.write("Text in unmerged cell.");
builder.insertCell();
builder.write("Text in unmerged cell.");
builder.endRow();
builder.endTable();

doc.save(base.artifactsDir + "CellFormat.horizontalMerge.docx");
```

### See Also

* module [Aspose.Words.Tables](../)

