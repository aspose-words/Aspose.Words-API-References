---
title: Font.emboss property
linktitle: emboss property
articleTitle: emboss property
second_title: Aspose.Words for Node.js
description: "Font.emboss property. True if the font is formatted as embossed."
type: docs
weight: 100
url: /nodejs-net/aspose.words/font/emboss/
---

## Font.emboss property

True if the font is formatted as embossed.


```js
get emboss(): boolean
```

### Examples

Shows how to apply engraving/embossing effects to text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.size = 36;
builder.font.color = "#ADD8E6";

// Below are two ways of using shadows to apply a 3D-like effect to the text.
// 1 -  Engrave text to make it look like the letters are sunken into the page:
builder.font.engrave = true;

builder.writeln("This text is engraved.");

// 2 -  Emboss text to make it look like the letters pop out of the page:
builder.font.engrave = false;
builder.font.emboss = true;

builder.writeln("This text is embossed.");

doc.save(base.artifactsDir + "Font.EngraveEmboss.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

