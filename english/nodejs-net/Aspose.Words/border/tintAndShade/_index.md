---
title: Border.tintAndShade property
linktitle: tintAndShade property
articleTitle: tintAndShade property
second_title: Aspose.Words for NodeJs
description: "Border.tintAndShade property. Gets or sets a double value that lightens or darkens a color."
type: docs
weight: 80
url: /nodejs-net/aspose.words/border/tintAndShade/
---

## Border.tintAndShade property

Gets or sets a double value that lightens or darkens a color.


```js
get tintAndShade(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws if you attempt to set this property to a value less than -1 or more than 1. |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if setting this property for Border object with non-theme colors. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.
Zero (0) is neutral.




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
* class [Border](../)

