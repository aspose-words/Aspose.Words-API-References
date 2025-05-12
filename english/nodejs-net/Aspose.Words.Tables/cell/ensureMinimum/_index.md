---
title: Cell.ensureMinimum method
linktitle: ensureMinimum method
articleTitle: ensureMinimum method
second_title: Aspose.Words for Node.js
description: "Cell.ensureMinimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 130
url: /nodejs-net/aspose.words.tables/cell/ensureMinimum/
---

## ensureMinimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```js
ensureMinimum()
```

### Examples

Shows how to ensure a cell node contains the nodes we need to begin adding content to it.

```js
let doc = new aw.Document();
let table = new aw.Tables.Table(doc);
doc.firstSection.body.appendChild(table);
let row = new aw.Tables.Row(doc);
table.appendChild(row);
let cell = new aw.Tables.Cell(doc);
row.appendChild(cell);

// Cells may contain paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new cell does not have any paragraphs, and we cannot add contents such as run and shape nodes to it until it does.
expect(cell.getChildNodes(aw.NodeType.Any, true).count).toEqual(0);

// Calling the "EnsureMinimum" method on a cell will ensure that
// the cell has at least one empty paragraph, which we can then add contents to.
cell.ensureMinimum();
cell.firstParagraph.appendChild(new aw.Run(doc, "Hello world!"));
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [Cell](../)

