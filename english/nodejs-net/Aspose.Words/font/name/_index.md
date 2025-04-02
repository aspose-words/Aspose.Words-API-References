---
title: Font.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "Font.name property. Gets or sets the name of the font."
type: docs
weight: 230
url: /nodejs-net/Aspose.Words/font/name/
---

## Font.name property

Gets or sets the name of the font.


```js
get name(): string
```

### Remarks

When getting, returns [Font.nameAscii](../nameAscii/).

When setting, sets [Font.nameAscii](../nameAscii/), [Font.nameBi](../nameBi/), [Font.nameFarEast](../nameFarEast/)
and [Font.nameOther](../nameOther/) to the specified value.




### Examples

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

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

