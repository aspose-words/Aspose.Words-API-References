---
title: Cell.nextCell property
linktitle: nextCell property
articleTitle: nextCell property
second_title: Aspose.Words for NodeJs
description: "Cell.nextCell property. Gets the next [Cell](../) node."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Tables/cell/nextCell/
---

## Cell.nextCell property

Gets the next [Cell](../) node.



```js
get nextCell(): Aspose.Words.Tables.Cell
```

### Remarks

The method can be used when you need to have typed access to cells of a [Row](../../row/). If a
[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node is found in a row instead of a cell, it is automatically
traversed to get a cell contained within.



### Examples

Shows how to enumerate through all table cells.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);

// Enumerate through all cells of the table.
for (let row = table.firstRow; row != null; row = row.nextRow)
{
  for (let cell = row.firstCell; cell != null; cell = cell.nextCell)
  {
    console.log(cell.getText());
  }
}
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [Cell](../)

