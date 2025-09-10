---
title: Shading class
linktitle: Shading class
articleTitle: Shading class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Shading class. Contains shading attributes for an object"
type: docs
weight: 1210
url: /nodejs-net/aspose.words/shading/
---

## Shading class

Contains shading attributes for an object.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




**Inheritance:** [Shading](./) → [InternableComplexAttr](../internablecomplexattr/)

### Properties

| Name | Description |
| --- | --- |
| [backgroundPatternColor](./backgroundPatternColor/) | Gets or sets the color that's applied to the background of the [Shading](./) object. |
| [backgroundPatternThemeColor](./backgroundPatternThemeColor/) | Gets or sets the background pattern theme color in the applied color scheme that is associated with this [Shading](./) object. |
| [backgroundTintAndShade](./backgroundTintAndShade/) | Gets or sets a double value that lightens or darkens a background theme color. |
| [foregroundPatternColor](./foregroundPatternColor/) | Gets or sets the color that's applied to the foreground of the [Shading](./) object. |
| [foregroundPatternThemeColor](./foregroundPatternThemeColor/) | Gets or sets the foreground pattern theme color in the applied color scheme that is associated with this [Shading](./) object. |
| [foregroundTintAndShade](./foregroundTintAndShade/) | Gets or sets a double value that lightens or darkens a foreground theme color. |
| [texture](./texture/) | Gets or sets the shading texture. |

### Methods

| Name | Description |
| --- | --- |
|[ clearFormatting()](./clearFormatting/#default) | Removes shading from the object. |
|[ equals(rhs)](./equals/#shading) | Determines whether the specified [Shading](./) is equal in value to the current [Shading](./). |

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

Shows how to decorate text with borders and shading.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let borders = builder.paragraphFormat.borders;
borders.distanceFromText = 20;
borders.at(aw.BorderType.Left).lineStyle = aw.LineStyle.Double;
borders.at(aw.BorderType.Right).lineStyle = aw.LineStyle.Double;
borders.at(aw.BorderType.Top).lineStyle = aw.LineStyle.Double;
borders.at(aw.BorderType.Bottom).lineStyle = aw.LineStyle.Double;

let shading = builder.paragraphFormat.shading;
shading.texture = aw.TextureIndex.TextureDiagonalCross;
shading.backgroundPatternColor = "#F08080";
shading.foregroundPatternColor = "#FFA07A";

builder.write("This paragraph is formatted with a double border and shading.");
doc.save(base.artifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### See Also

* module [Aspose.Words](../)
* class [InternableComplexAttr](../internablecomplexattr/)

