---
title: ParagraphFormat.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.borders property. Gets collection of borders of the paragraph."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words/paragraphformat/borders/
---

## ParagraphFormat.borders property

Gets collection of borders of the paragraph.


```js
get borders(): Aspose.Words.BorderCollection
```

### Examples

Shows how to insert a paragraph with a top border.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let topBorder = builder.paragraphFormat.borders.top;
topBorder.lineWidth = 4.0;
topBorder.lineStyle = aw.LineStyle.DashSmallGap;
// Set ThemeColor only when LineWidth or LineStyle setted.
topBorder.themeColor = aw.Themes.ThemeColor.Accent1;
topBorder.tintAndShade = 0.25;

builder.writeln("Text with a top border.");

doc.save(base.artifactsDir + "Border.ParagraphTopBorder.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

