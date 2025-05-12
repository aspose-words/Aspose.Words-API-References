---
title: Table.setShading method
linktitle: setShading method
articleTitle: setShading method
second_title: Aspose.Words for Node.js
description: "Table.setShading method. Sets shading to the specified values on whole table."
type: docs
weight: 420
url: /nodejs-net/aspose.words/table/setShading/
---

## setShading(texture, foregroundColor, backgroundColor) {#textureindex_string_string}

Sets shading to the specified values on whole table.


```js
setShading(texture: Aspose.Words.TextureIndex, foregroundColor: string, backgroundColor: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| texture | [TextureIndex](../../textureindex/) | The texture to apply. |
| foregroundColor | string | The color of the texture. |
| backgroundColor | string | The color of the background fill. |

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

