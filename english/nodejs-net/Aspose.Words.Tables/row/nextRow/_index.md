---
title: Row.nextRow property
linktitle: nextRow property
articleTitle: nextRow property
second_title: Aspose.Words for NodeJs
description: "Row.nextRow property. Gets the next [Row](../) node."
type: docs
weight: 70
url: /nodejs-net/aspose.words.tables/row/nextRow/
---

## Row.nextRow property

Gets the next [Row](../) node.



```js
get nextRow(): Aspose.Words.Tables.Row
```

### Remarks

The method can be used when you need to have typed access to table rows. If a
[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node is found in a table instead of a row,
it is automatically traversed to get a row contained within.



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
* class [Row](../)

