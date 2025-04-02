---
title: Table.absoluteHorizontalDistance property
linktitle: absoluteHorizontalDistance property
articleTitle: absoluteHorizontalDistance property
second_title: Aspose.Words for NodeJs
description: "Table.absoluteHorizontalDistance property. Gets or sets absolute horizontal floating table position specified by the table properties, in points"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/table/absoluteHorizontalDistance/
---

## Table.absoluteHorizontalDistance property

Gets or sets absolute horizontal floating table position specified by the table properties, in points.
Default value is 0.


```js
get absoluteHorizontalDistance(): number
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

