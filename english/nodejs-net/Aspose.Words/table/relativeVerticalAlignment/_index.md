---
title: Table.relativeVerticalAlignment property
linktitle: relativeVerticalAlignment property
articleTitle: relativeVerticalAlignment property
second_title: Aspose.Words for Node.js
description: "Table.relativeVerticalAlignment property. Gets or sets floating table relative vertical alignment."
type: docs
weight: 240
url: /nodejs-net/aspose.words/table/relativeVerticalAlignment/
---

## Table.relativeVerticalAlignment property

Gets or sets floating table relative vertical alignment.


```js
get relativeVerticalAlignment(): Aspose.Words.Drawing.VerticalAlignment
```

### Examples

Shows how set the location of floating tables.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Table 1, cell 1");
builder.endTable();
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(300);

// Set the table's location to a place on the page, such as, in this case, the bottom right corner.
table.relativeVerticalAlignment = aw.Drawing.VerticalAlignment.Bottom;
table.relativeHorizontalAlignment = aw.Drawing.HorizontalAlignment.Right;

table = builder.startTable();
builder.insertCell();
builder.write("Table 2, cell 1");
builder.endTable();
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(300);

// We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table. 
table.absoluteVerticalDistance = 50;
table.absoluteHorizontalDistance = 100;

doc.save(base.artifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

