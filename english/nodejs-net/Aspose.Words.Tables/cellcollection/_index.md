---
title: CellCollection class
linktitle: CellCollection class
articleTitle: CellCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.CellCollection class. Provides typed access to a collection of [Cell](../cell/) nodes"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Tables/cellcollection/
---

## CellCollection class

Provides typed access to a collection of [Cell](../cell/) nodes.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




**Inheritance:** [CellCollection](./) → [NodeCollection](../../Aspose.Words/nodecollection/)

### Properties

| Name | Description |
| --- | --- |
| [count](../../Aspose.Words/nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
| [this[]](../../Aspose.Words/nodecollection/this[]/) | <br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../../Aspose.Words/nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ clear()](../../Aspose.Words/nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ contains(node)](../../Aspose.Words/nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ indexOf(node)](../../Aspose.Words/nodecollection/indexOf/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ insert(index, node)](../../Aspose.Words/nodecollection/insert/#number_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ remove(node)](../../Aspose.Words/nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ removeAt(index)](../../Aspose.Words/nodecollection/removeAt/#number) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../../Aspose.Words/nodecollection/)) |
|[ toArray()](./toArray/#default) | Copies all cells from the collection to a new array of cells. |

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

* module [Aspose.Words.Tables](../)
* class [NodeCollection](../../Aspose.Words/nodecollection/)

