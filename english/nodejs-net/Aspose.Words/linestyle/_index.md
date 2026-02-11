---
title: LineStyle enumeration
linktitle: LineStyle enumeration
articleTitle: LineStyle enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.LineStyle enumeration. Specifies line style of a [Border](../border/)."
type: docs
weight: 800
url: /nodejs-net/aspose.words/linestyle/
---

## LineStyle enumeration

Specifies line style of a [Border](../border/).



### Members

| Name | Description |
| --- | --- |
| None |  |
| Single |  |
| Thick |  |
| Double |  |
| Hairline |  |
| Dot |  |
| DashLargeGap |  |
| DotDash |  |
| DotDotDash |  |
| Triple |  |
| ThinThickSmallGap |  |
| ThickThinSmallGap |  |
| ThinThickThinSmallGap |  |
| ThinThickMediumGap |  |
| ThickThinMediumGap |  |
| ThinThickThinMediumGap |  |
| ThinThickLargeGap |  |
| ThickThinLargeGap |  |
| ThinThickThinLargeGap |  |
| Wave |  |
| DoubleWave |  |
| DashSmallGap |  |
| DashDotStroker |  |
| Emboss3D |  |
| Engrave3D |  |
| Outset |  |
| Inset |  |

### Examples

Shows how to insert a string surrounded by a border into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.border.color = "#008000";
builder.font.border.lineWidth = 2.5;
builder.font.border.lineStyle = aw.LineStyle.DashDotStroker;

builder.write("Text surrounded by green border.");

doc.save(base.artifactsDir + "Border.FontBorder.docx");
```

### See Also

* module [Aspose.Words](../)

