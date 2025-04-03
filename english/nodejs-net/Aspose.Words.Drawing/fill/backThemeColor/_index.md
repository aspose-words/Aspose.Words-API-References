---
title: Fill.backThemeColor property
linktitle: backThemeColor property
articleTitle: backThemeColor property
second_title: Aspose.Words for NodeJs
description: "Fill.backThemeColor property. Gets or sets a ThemeColor object that represents the background color for the fill."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing/fill/backThemeColor/
---

## Fill.backThemeColor property

Gets or sets a ThemeColor object that represents the background color for the fill.


```js
get backThemeColor(): Aspose.Words.Themes.ThemeColor
```

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

