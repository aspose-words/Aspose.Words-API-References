---
title: Shading.backgroundTintAndShade property
linktitle: backgroundTintAndShade property
articleTitle: backgroundTintAndShade property
second_title: Aspose.Words for NodeJs
description: "Shading.backgroundTintAndShade property. Gets or sets a double value that lightens or darkens a background theme color."
type: docs
weight: 30
url: /nodejs-net/aspose.words/shading/backgroundTintAndShade/
---

## Shading.backgroundTintAndShade property

Gets or sets a double value that lightens or darkens a background theme color.


```js
get backgroundTintAndShade(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if set this property for Shading object with non-theme colors. |

### Remarks

The allowed values are in the range from -1 (the darkest) to 1 (the lightest) for this property.

Zero (0) is neutral.




### Examples

Shows how to set foreground and background colors for shading texture.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shading = doc.firstSection.body.firstParagraph.paragraphFormat.shading;
shading.texture = aw.TextureIndex.Texture12Pt5Percent;
shading.foregroundPatternThemeColor = aw.Themes.ThemeColor.Dark1;
shading.backgroundPatternThemeColor = aw.Themes.ThemeColor.Dark2;

shading.foregroundTintAndShade = 0.5;
shading.backgroundTintAndShade = -0.2;

builder.font.border.color = "#008000";
builder.font.border.lineWidth = 2.5;
builder.font.border.lineStyle = aw.LineStyle.DashDotStroker;

builder.writeln("Foreground and background pattern colors for shading texture.");

doc.save(base.artifactsDir + "Font.ForegroundAndBackground.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Shading](../)

