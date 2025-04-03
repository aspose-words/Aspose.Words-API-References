---
title: Shading.backgroundPatternThemeColor property
linktitle: backgroundPatternThemeColor property
articleTitle: backgroundPatternThemeColor property
second_title: Aspose.Words for NodeJs
description: "Shading.backgroundPatternThemeColor property. Gets or sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../) object."
type: docs
weight: 20
url: /nodejs-net/aspose.words/shading/backgroundPatternThemeColor/
---

## Shading.backgroundPatternThemeColor property

Gets or sets the background pattern theme color in the applied color scheme that is associated with this [Shading](../) object.



```js
get backgroundPatternThemeColor(): Aspose.Words.Themes.ThemeColor
```

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

