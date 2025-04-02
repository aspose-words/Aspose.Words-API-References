---
title: Table.allowAutoFit property
linktitle: allowAutoFit property
articleTitle: allowAutoFit property
second_title: Aspose.Words for NodeJs
description: "Table.allowAutoFit property. Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/table/allowAutoFit/
---

## Table.allowAutoFit property

Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.


```js
get allowAutoFit(): boolean
```

### Remarks

The default value is ``True``.




### Examples

Shows how to enable/disable automatic table cell resizing.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.cellFormat.preferredWidth = aw.Tables.PreferredWidth.fromPoints(100);
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
      "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.insertCell();
builder.cellFormat.preferredWidth = aw.Tables.PreferredWidth.auto;
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
      "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.endRow();
builder.endTable();

// Set the "AllowAutoFit" property to "false" to get the table to maintain the dimensions
// of all its rows and cells, and truncate contents if they get too large to fit.
// Set the "AllowAutoFit" property to "true" to allow the table to change its cells' width and height
// to accommodate their contents.
table.allowAutoFit = allowAutoFit;

doc.save(base.artifactsDir + "Table.AllowAutoFitOnTable.html");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)
* method [Table.autoFit()](../autoFit/#autofitbehavior)

