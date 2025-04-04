---
title: Row.ensureMinimum method
linktitle: ensureMinimum method
articleTitle: ensureMinimum method
second_title: Aspose.Words for Node.js
description: "Row.ensureMinimum method. If the [Row](../) has no cells, creates and appends one [Cell](../../cell/)."
type: docs
weight: 150
url: /nodejs-net/aspose.words.tables/row/ensureMinimum/
---

## ensureMinimum() {#default}

If the [Row](../) has no cells, creates and appends one [Cell](../../cell/).



```js
ensureMinimum()
```

### Examples

Shows how to ensure a row node contains the nodes we need to begin adding content to it.

```js
let doc = new aw.Document();
let table = new aw.Tables.Table(doc);
doc.firstSection.body.appendChild(table);
let row = new aw.Tables.Row(doc);
table.appendChild(row);

// Rows contain cells, containing paragraphs with typical elements such as runs, shapes, and even other tables.
// Our new row has none of these nodes, and we cannot add contents to it until it does.
expect(row.getChildNodes(aw.NodeType.Any, true).count).toEqual(0);

// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one cell with an empty paragraph.
row.ensureMinimum();
row.firstCell.firstParagraph.appendChild(new aw.Run(doc, "Hello world!"));
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [Row](../)

