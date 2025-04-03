---
title: CellCollection.toArray method
linktitle: toArray method
articleTitle: toArray method
second_title: Aspose.Words for NodeJs
description: "CellCollection.toArray method. Copies all cells from the collection to a new array of cells."
type: docs
weight: 10
url: /nodejs-net/aspose.words.tables/cellcollection/toArray/
---

## toArray() {#default}

Copies all cells from the collection to a new array of cells.


```js
toArray()
```

### Returns

An array of cells.


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
* class [CellCollection](../)

