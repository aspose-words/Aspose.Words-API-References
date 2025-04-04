---
title: TextureIndex enumeration
linktitle: TextureIndex enumeration
articleTitle: TextureIndex enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TextureIndex enumeration. Specifies shading texture."
type: docs
weight: 1420
url: /nodejs-net/aspose.words/textureindex/
---

## TextureIndex enumeration

Specifies shading texture.


### Members

| Name | Description |
| --- | --- |
| Texture10Percent |  |
| Texture12Pt5Percent |  |
| Texture15Percent |  |
| Texture17Pt5Percent |  |
| Texture20Percent |  |
| Texture22Pt5Percent |  |
| Texture25Percent |  |
| Texture27Pt5Percent |  |
| Texture2Pt5Percent |  |
| Texture30Percent |  |
| Texture32Pt5Percent |  |
| Texture35Percent |  |
| Texture37Pt5Percent |  |
| Texture40Percent |  |
| Texture42Pt5Percent |  |
| Texture45Percent |  |
| Texture47Pt5Percent |  |
| Texture50Percent |  |
| Texture52Pt5Percent |  |
| Texture55Percent |  |
| Texture57Pt5Percent |  |
| Texture5Percent |  |
| Texture60Percent |  |
| Texture62Pt5Percent |  |
| Texture65Percent |  |
| Texture67Pt5Percent |  |
| Texture70Percent |  |
| Texture72Pt5Percent |  |
| Texture75Percent |  |
| Texture77Pt5Percent |  |
| Texture7Pt5Percent |  |
| Texture80Percent |  |
| Texture82Pt5Percent |  |
| Texture85Percent |  |
| Texture87Pt5Percent |  |
| Texture90Percent |  |
| Texture92Pt5Percent |  |
| Texture95Percent |  |
| Texture97Pt5Percent |  |
| TextureCross |  |
| TextureDarkCross |  |
| TextureDarkDiagonalCross |  |
| TextureDarkDiagonalDown |  |
| TextureDarkDiagonalUp |  |
| TextureDarkHorizontal |  |
| TextureDarkVertical |  |
| TextureDiagonalCross |  |
| TextureDiagonalDown |  |
| TextureDiagonalUp |  |
| TextureHorizontal |  |
| TextureNone |  |
| TextureSolid |  |
| TextureVertical |  |
| TextureNil | Specifies that there shall be no pattern used on the current shaded region  (i.e. the pattern shall be a complete fill with the background color). |

### Examples

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

* module [Aspose.Words](../)

