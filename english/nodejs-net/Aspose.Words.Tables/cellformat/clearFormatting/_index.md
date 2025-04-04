---
title: CellFormat.clearFormatting method
linktitle: clearFormatting method
articleTitle: clearFormatting method
second_title: Aspose.Words for Node.js
description: "CellFormat.clearFormatting method. Resets to default cell formatting"
type: docs
weight: 160
url: /nodejs-net/aspose.words.tables/cellformat/clearFormatting/
---

## clearFormatting() {#default}

Resets to default cell formatting. Does not change the width of the cell.


```js
clearFormatting()
```

### Examples

Shows how to combine the rows from two tables into one.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
let firstTable = doc.firstSection.body.tables.at(0);

// 2 -  Using the "GetChild" method:
let secondTable = doc.getTable(1, true);

// Append all rows from the current table to the next.
while (secondTable.hasChildNodes)
  firstTable.rows.add(secondTable.firstRow);

// Remove the empty table container.
secondTable.remove();

doc.save(base.artifactsDir + "Table.CombineTables.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [CellFormat](../)

