---
title: Font.autoColor property
linktitle: autoColor property
articleTitle: autoColor property
second_title: Aspose.Words for NodeJs
description: "Font.autoColor property. Returns the present calculated color of the text (black or white) to be used for 'auto color'"
type: docs
weight: 20
url: /nodejs-net/aspose.words/font/autoColor/
---

## Font.autoColor property

Returns the present calculated color of the text (black or white) to be used for 'auto color'.
If the color is not 'auto' then returns [Font.color](../color/).



```js
get autoColor(): string
```

### Remarks

When text has 'automatic color', the actual color of text is calculated automatically
so that it is readable against the background color. As you change the background color,
the text color will automatically switch to black or white in MS Word to maximize legibility.




### Examples

Shows how to improve readability by automatically selecting text color based on the brightness of its background.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// If a run's Font object does not specify text color, it will automatically
// select either black or white depending on the background color's color.
expect(builder.font.color).toEqual("#000000");

// The default color for text is black. If the color of the background is dark, black text will be difficult to see.
// To solve this problem, the AutoColor property will display this text in white.
builder.font.shading.backgroundPatternColor = "#00008B";

builder.writeln("The text color automatically chosen for this run is white.");

expect(doc.firstSection.body.paragraphs.at(0).runs.at(0).font.autoColor).toEqual("#FFFFFF");

// If we change the background to a light color, black will be a more
// suitable text color than white so that the auto color will display it in black.
builder.font.shading.backgroundPatternColor = "#ADD8E6";

builder.writeln("The text color automatically chosen for this run is black.");

expect(doc.firstSection.body.paragraphs.at(1).runs.at(0).font.autoColor).toEqual("#000000");

doc.save(base.artifactsDir + "Font.SetFontAutoColor.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

