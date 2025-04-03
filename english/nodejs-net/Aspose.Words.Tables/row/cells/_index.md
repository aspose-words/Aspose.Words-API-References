---
title: Row.cells property
linktitle: cells property
articleTitle: cells property
second_title: Aspose.Words for NodeJs
description: "Row.cells property. Provides typed access to the [Cell](../../cell/) child nodes of the row."
type: docs
weight: 20
url: /nodejs-net/aspose.words.tables/row/cells/
---

## Row.cells property

Provides typed access to the [Cell](../../cell/) child nodes of the row.



```js
get cells(): Aspose.Words.Tables.CellCollection
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

### See Also

* module [Aspose.Words.Tables](../../)
* class [Row](../)

