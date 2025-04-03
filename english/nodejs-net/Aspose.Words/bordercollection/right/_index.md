---
title: BorderCollection.right property
linktitle: right property
articleTitle: right property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.right property. Gets the right border."
type: docs
weight: 90
url: /nodejs-net/aspose.words/bordercollection/right/
---

## BorderCollection.right property

Gets the right border.


```js
get right(): Aspose.Words.Border
```

### Examples

Shows how to apply border and shading color while building a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Start a table and set a default color/thickness for its borders.
let table = builder.startTable();
table.setBorders(aw.LineStyle.Single, 2.0, "#000000");

// Create a row with two cells with different background colors.
builder.insertCell();
builder.cellFormat.shading.backgroundPatternColor = "#87CEFA";
builder.writeln("Row 1, Cell 1.");
builder.insertCell();
builder.cellFormat.shading.backgroundPatternColor = "#FFA500";
builder.writeln("Row 1, Cell 2.");
builder.endRow();

// Reset cell formatting to disable the background colors
// set a custom border thickness for all new cells created by the builder,
// then build a second row.
builder.cellFormat.clearFormatting();
builder.cellFormat.borders.left.lineWidth = 4.0;
builder.cellFormat.borders.right.lineWidth = 4.0;
builder.cellFormat.borders.top.lineWidth = 4.0;
builder.cellFormat.borders.bottom.lineWidth = 4.0;

builder.insertCell();
builder.writeln("Row 2, Cell 1.");
builder.insertCell();
builder.writeln("Row 2, Cell 2.");

doc.save(base.artifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [BorderCollection](../)

