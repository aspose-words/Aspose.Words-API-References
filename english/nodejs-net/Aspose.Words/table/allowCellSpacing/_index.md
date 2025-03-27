---
title: Table.allowCellSpacing property
linktitle: allowCellSpacing property
articleTitle: allowCellSpacing property
second_title: Aspose.Words for NodeJs
description: "Table.allowCellSpacing property. Gets or sets the Allow spacing between cells option."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/table/allowCellSpacing/
---

## Table.allowCellSpacing property

Gets or sets the "Allow spacing between cells" option.


```js
get allowCellSpacing(): boolean
```

### Examples

Shows how to enable spacing between individual cells in a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Animal");
builder.insertCell();
builder.write("Class");
builder.endRow();
builder.insertCell();
builder.write("Dog");
builder.insertCell();
builder.write("Mammal");
builder.endTable();

table.cellSpacing = 3;

// Set the "AllowCellSpacing" property to "true" to enable spacing between cells
// with a magnitude equal to the value of the "CellSpacing" property, in points.
// Set the "AllowCellSpacing" property to "false" to disable cell spacing
// and ignore the value of the "CellSpacing" property.
table.allowCellSpacing = allowCellSpacing;

doc.save(base.artifactsDir + "Table.allowCellSpacing.html");

// Adjusting the "CellSpacing" property will automatically enable cell spacing.
table.cellSpacing = 5;

expect(table.allowCellSpacing).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

