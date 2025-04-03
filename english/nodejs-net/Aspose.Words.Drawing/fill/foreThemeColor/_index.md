---
title: Fill.foreThemeColor property
linktitle: foreThemeColor property
articleTitle: foreThemeColor property
second_title: Aspose.Words for NodeJs
description: "Fill.foreThemeColor property. Gets or sets a ThemeColor object that represents the foreground color for the fill."
type: docs
weight: 80
url: /nodejs-net/aspose.words.drawing/fill/foreThemeColor/
---

## Fill.foreThemeColor property

Gets or sets a ThemeColor object that represents the foreground color for the fill.


```js
get foreThemeColor(): Aspose.Words.Themes.ThemeColor
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

