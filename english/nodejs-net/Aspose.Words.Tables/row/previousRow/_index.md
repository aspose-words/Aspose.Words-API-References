---
title: Row.previousRow property
linktitle: previousRow property
articleTitle: previousRow property
second_title: Aspose.Words for Node.js
description: "Row.previousRow property. Gets the previous [Row](../) node."
type: docs
weight: 100
url: /nodejs-net/aspose.words.tables/row/previousRow/
---

## Row.previousRow property

Gets the previous [Row](../) node.



```js
get previousRow(): Aspose.Words.Tables.Row
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

