---
title: Font.size property
linktitle: size property
articleTitle: size property
second_title: Aspose.Words for NodeJs
description: "Font.size property. Gets or sets the font size in points."
type: docs
weight: 350
url: /nodejs-net/Aspose.Words/font/size/
---

## Font.size property

Gets or sets the font size in points.


```js
get size(): number
```

### Examples

Shows how to format a run of text using its font property.

```js
let doc = new aw.Document();
let run = new aw.Run(doc, "Hello world!");

let font = run.font;
font.name = "Courier New";
font.size = 36;
font.highlightColor = "#FFFF00";

doc.firstSection.body.firstParagraph.appendChild(run);
doc.save(base.artifactsDir + "Font.CreateFormattedRun.docx");
```

Shows how to insert formatted text using DocumentBuilder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Specify font formatting, then add text.
let font = builder.font;
font.size = 16;
font.bold = true;
font.color = "#0000FF";
font.name = "Courier New";
font.underline = aw.Underline.Dash;

builder.write("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

