---
title: TextOrientation enumeration
linktitle: TextOrientation enumeration
articleTitle: TextOrientation enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TextOrientation enumeration. Specifies orientation of text on a page, in a table cell or a text frame."
type: docs
weight: 1400
url: /nodejs-net/aspose.words/textorientation/
---

## TextOrientation enumeration

Specifies orientation of text on a page, in a table cell or a text frame.


### Members

| Name | Description |
| --- | --- |
| Horizontal | Text is arranged horizontally (lr-tb). |
| Downward | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| Upward | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| HorizontalRotatedFarEast | Text is arranged horizontally, but Far East characters are rotated 90 degrees to the left (lr-tb-v). |
| VerticalFarEast | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VerticalRotatedFarEast | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally  (tb-lr-v). |

### Examples

Shows how to build a formatted 2x2 table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.cellFormat.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;
builder.write("Row 1, cell 1.");
builder.insertCell();
builder.write("Row 1, cell 2.");
builder.endRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
expect(table.rows.at(0).cells.at(0).cellFormat.verticalAlignment).toEqual(aw.Tables.CellVerticalAlignment.Center);
expect(table.rows.at(0).cells.at(1).cellFormat.verticalAlignment).toEqual(aw.Tables.CellVerticalAlignment.Center);

builder.insertCell();
builder.rowFormat.height = 100;
builder.rowFormat.heightRule = aw.HeightRule.Exactly;
builder.cellFormat.orientation = aw.TextOrientation.Upward;
builder.write("Row 2, cell 1.");
builder.insertCell();
builder.cellFormat.orientation = aw.TextOrientation.Downward;
builder.write("Row 2, cell 2.");
builder.endRow();
builder.endTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
expect(table.rows.at(0).rowFormat.height).toEqual(0);
expect(table.rows.at(0).rowFormat.heightRule).toEqual(aw.HeightRule.Auto);
expect(table.rows.at(1).rowFormat.height).toEqual(100);
expect(table.rows.at(1).rowFormat.heightRule).toEqual(aw.HeightRule.Exactly);
expect(table.rows.at(1).cells.at(0).cellFormat.orientation).toEqual(aw.TextOrientation.Upward);
expect(table.rows.at(1).cells.at(1).cellFormat.orientation).toEqual(aw.TextOrientation.Downward);

doc.save(base.artifactsDir + "DocumentBuilder.BuildTable.docx");
```

### See Also

* module [Aspose.Words](../)

