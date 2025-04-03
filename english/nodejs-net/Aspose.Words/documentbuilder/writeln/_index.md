---
title: DocumentBuilder.writeln method
linktitle: writeln method
articleTitle: writeln method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.writeln method"
type: docs
weight: 700
url: /nodejs-net/aspose.words/documentbuilder/writeln/
---

## writeln(text) {#string}

Inserts a string and a paragraph break into the document.


```js
writeln(text: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | string | The string to insert into the document. |

### Remarks

Current font and paragraph formatting specified by the [DocumentBuilder.font](../font/) and [DocumentBuilder.paragraphFormat](../paragraphFormat/) properties are used.



## writeln() {#default}

Inserts a paragraph break into the document.


```js
writeln()
```

### Remarks

Calls [DocumentBuilder.insertParagraph()](../insertParagraph/#default).




## Examples

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

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

