---
title: Border.themeColor property
linktitle: themeColor property
articleTitle: themeColor property
second_title: Aspose.Words for NodeJs
description: "Border.themeColor property. Gets or sets the theme color in the applied color scheme that is associated with this Border object."
type: docs
weight: 70
url: /nodejs-net/aspose.words/border/themeColor/
---

## Border.themeColor property

Gets or sets the theme color in the applied color scheme that is associated with this Border object.


```js
get themeColor(): Aspose.Words.Themes.ThemeColor
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
* class [Border](../)

