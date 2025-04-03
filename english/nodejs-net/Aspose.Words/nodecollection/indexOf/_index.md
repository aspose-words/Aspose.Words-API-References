---
title: NodeCollection.indexOf method
linktitle: indexOf method
articleTitle: indexOf method
second_title: Aspose.Words for NodeJs
description: "NodeCollection.indexOf method. Returns the zero-based index of the specified node."
type: docs
weight: 60
url: /nodejs-net/aspose.words/nodecollection/indexOf/
---

## indexOf(node) {#node}

Returns the zero-based index of the specified node.


```js
indexOf(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to locate. |

### Remarks

This method performs a linear search; therefore, the average execution time is proportional to [NodeCollection.count](../count/).




### Returns

The zero-based index of the node within the collection, if found; otherwise, -1.


### Examples

Shows how to get the index of a node in a collection.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

let table = doc.firstSection.body.tables.at(0);
let allTables = doc.getChildNodes(aw.NodeType.Table, true);

expect(allTables.indexOf(table)).toEqual(0);

let row = table.rows.at(2);

expect(table.indexOf(row)).toEqual(2);

let cell = row.lastCell;

expect(row.indexOf(cell)).toEqual(4);
```

### See Also

* module [Aspose.Words](../../)
* class [NodeCollection](../)

