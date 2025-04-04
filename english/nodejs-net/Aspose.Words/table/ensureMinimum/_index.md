---
title: Table.ensureMinimum method
linktitle: ensureMinimum method
articleTitle: ensureMinimum method
second_title: Aspose.Words for Node.js
description: "Table.ensureMinimum method. If the table has no rows, creates and appends one [Row](../../../aspose.words.tables/row/)."
type: docs
weight: 420
url: /nodejs-net/aspose.words/table/ensureMinimum/
---

## ensureMinimum() {#default}

If the table has no rows, creates and appends one [Row](../../../aspose.words.tables/row/).



```js
ensureMinimum()
```

### Examples

Shows how to ensure that a table node contains the nodes we need to add content.

```js
let doc = new aw.Document();
let table = new aw.Tables.Table(doc);
doc.firstSection.body.appendChild(table);

// Tables contain rows, which contain cells, which may contain paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Our new table has none of these nodes, and we cannot add contents to it until it does.
expect(table.getChildNodes(aw.NodeType.Any, true).count).toEqual(0);

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row and one cell with an empty paragraph.
table.ensureMinimum();
table.firstRow.firstCell.firstParagraph.appendChild(new aw.Run(doc, "Hello world!"));
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

