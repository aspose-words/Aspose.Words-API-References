---
title: Table.firstRow property
linktitle: firstRow property
articleTitle: firstRow property
second_title: Aspose.Words for NodeJs
description: "Table.firstRow property. Returns the first [Row](../../../Aspose.Words.Tables/row/) node in the table."
type: docs
weight: 160
url: /nodejs-net/Aspose.Words/table/firstRow/
---

## Table.firstRow property

Returns the first [Row](../../../Aspose.Words.Tables/row/) node in the table.



```js
get firstRow(): Aspose.Words.Tables.Row
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

Shows how to remove the first and last rows of all tables in a document.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

let tables = doc.firstSection.body.tables.toArray();

expect(tables[0].rows.count).toEqual(5);
expect(tables[1].rows.count).toEqual(4);

for (var table of tables)
{
  table.firstRow?.remove();
  table.lastRow?.remove();
}

expect(tables[0].rows.count).toEqual(3);
expect(tables[1].rows.count).toEqual(2);
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

