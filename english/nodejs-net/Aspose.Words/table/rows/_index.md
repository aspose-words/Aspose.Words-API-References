---
title: Table.rows property
linktitle: rows property
articleTitle: rows property
second_title: Aspose.Words for Node.js
description: "Table.rows property. Provides typed access to the rows of the table."
type: docs
weight: 260
url: /nodejs-net/aspose.words/table/rows/
---

## Table.rows property

Provides typed access to the rows of the table.


```js
get rows(): Aspose.Words.Tables.RowCollection
```

### Examples

Shows how to iterate through all tables in the document and print the contents of each cell.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let tables = doc.firstSection.body.tables;

expect(tables.toArray().length).toEqual(2);

for (let i = 0; i < tables.count; i++)
{
  console.log(`Start of Table ${i}`);

  let rows = tables.at(i).rows;

  for (let j = 0; j < rows.count; j++)
  {
    console.log(`\tStart of Row ${j}`);

    let cells = rows.at(j).cells;

    for (let k = 0; k < cells.count; k++)
    {
      let cellText = cells.at(k).toString(aw.SaveFormat.Text).trim();
      console.log(`\t\tContents of Cell:${k} = \"${cellText}\"`);
    }

    console.log(`\tEnd of Row ${j}`);
  }

  console.log(`End of Table ${i}\n`);
}
```

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

* module [Aspose.Words](../../)
* class [Table](../)

