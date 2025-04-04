---
title: CompositeNode.hasChildNodes property
linktitle: hasChildNodes property
articleTitle: hasChildNodes property
second_title: Aspose.Words for Node.js
description: "CompositeNode.hasChildNodes property. Returns ``true`` if this node has any child nodes."
type: docs
weight: 30
url: /nodejs-net/aspose.words/compositenode/hasChildNodes/
---

## CompositeNode.hasChildNodes property

Returns ``true`` if this node has any child nodes.



```js
get hasChildNodes(): boolean
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

* module [Aspose.Words](../../)
* class [CompositeNode](../)

