---
title: TableAlignment enumeration
linktitle: TableAlignment enumeration
articleTitle: TableAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Tables.TableAlignment enumeration. Specifies alignment for an inline table."
type: docs
weight: 120
url: /nodejs-net/aspose.words.tables/tablealignment/
---

## TableAlignment enumeration

Specifies alignment for an inline table.


### Members

| Name | Description |
| --- | --- |
| Left | The table is aligned to the left. |
| Center | The table is centered. |
| Right | The table is aligned to the right. |

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

* module [Aspose.Words.Tables](../)

