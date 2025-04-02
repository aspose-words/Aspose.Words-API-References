---
title: Table.rightPadding property
linktitle: rightPadding property
articleTitle: rightPadding property
second_title: Aspose.Words for NodeJs
description: "Table.rightPadding property. Gets or sets the amount of space (in points) to add to the right of the contents of cells."
type: docs
weight: 250
url: /nodejs-net/Aspose.Words/table/rightPadding/
---

## Table.rightPadding property

Gets or sets the amount of space (in points) to add to the right of the contents of cells.


```js
get rightPadding(): number
```

### Examples

Shows how to configure content padding in a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1.");
builder.insertCell();
builder.write("Row 1, cell 2.");
builder.endTable();

// For every cell in the table, set the distance between its contents and each of its borders. 
// This table will maintain the minimum padding distance by wrapping text.
table.leftPadding = 30;
table.rightPadding = 60;
table.topPadding = 10;
table.bottomPadding = 90;
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(250);

doc.save(base.artifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

