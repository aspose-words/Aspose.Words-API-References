---
title: Table.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for NodeJs
description: "Table.alignment property. Specifies how an inline table is aligned in the document."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/table/alignment/
---

## Table.alignment property

Specifies how an inline table is aligned in the document.


```js
get alignment(): Aspose.Words.Tables.TableAlignment
```

### Remarks

The default value is [TableAlignment.Left](../../../aspose.words.tables/tablealignment/#Left).




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

