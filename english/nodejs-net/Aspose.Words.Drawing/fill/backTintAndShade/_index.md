---
title: Fill.backTintAndShade property
linktitle: backTintAndShade property
articleTitle: backTintAndShade property
second_title: Aspose.Words for Node.js
description: "Fill.backTintAndShade property. Gets or sets a double value that lightens or darkens the background color."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing/fill/backTintAndShade/
---

## Fill.backTintAndShade property

Gets or sets a double value that lightens or darkens the background color.


```js
get backTintAndShade(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.




### Examples

Shows how to set theme color for foreground/background shape color.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertShape(aw.Drawing.ShapeType.RoundRectangle, 80, 80);

let fill = shape.fill;
fill.foreThemeColor = aw.Themes.ThemeColor.Dark1;
fill.backThemeColor = aw.Themes.ThemeColor.Background2;

// Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
if (fill.backTintAndShade == 0)
  fill.backTintAndShade = 0.2;

doc.save(base.artifactsDir + "Shape.FillThemeColor.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

