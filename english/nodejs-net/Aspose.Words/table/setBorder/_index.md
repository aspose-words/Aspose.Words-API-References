---
title: Table.setBorder method
linktitle: setBorder method
articleTitle: setBorder method
second_title: Aspose.Words for NodeJs
description: "Table.setBorder method. Sets the specified table border to the specified line style, width and color."
type: docs
weight: 430
url: /nodejs-net/aspose.words/table/setBorder/
---

## setBorder(borderType, lineStyle, lineWidth, color, isOverrideCellBorders) {#bordertype_linestyle_number_string_boolean}

Sets the specified table border to the specified line style, width and color.


```js
setBorder(borderType: Aspose.Words.BorderTypelineStyle: Aspose.Words.LineStylelineWidth: numbercolor: stringisOverrideCellBorders: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| borderType | [BorderType](../../bordertype/) | The table border to change. |
| lineStyle | [LineStyle](../../linestyle/) | The line style to apply. |
| lineWidth | number | The line width to set (in points). |
| color | string | The color to use for the border. |
| isOverrideCellBorders | boolean | When ``true``, causes all existing explicit cell borders to be removed. |

### Examples

Shows how to apply an outline border to a table.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let table = doc.firstSection.body.tables.at(0);

// Align the table to the center of the page.
table.alignment = aw.Tables.TableAlignment.Center;

// Clear any existing borders and shading from the table.
table.clearBorders();
table.clearShading();

// Add green borders to the outline of the table.
table.setBorder(aw.BorderType.Left, aw.LineStyle.Single, 1.5, "#008000", true);
table.setBorder(aw.BorderType.Right, aw.LineStyle.Single, 1.5, "#008000", true);
table.setBorder(aw.BorderType.Top, aw.LineStyle.Single, 1.5, "#008000", true);
table.setBorder(aw.BorderType.Bottom, aw.LineStyle.Single, 1.5, "#008000", true);

// Fill the cells with a light green solid color.
table.setShading(aw.TextureIndex.TextureSolid, "#90EE90", "#000000");

doc.save(base.artifactsDir + "Table.SetOutlineBorders.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

