---
title: Font.engrave property
linktitle: engrave property
articleTitle: engrave property
second_title: Aspose.Words for NodeJs
description: "Font.engrave property. True if the font is formatted as engraved."
type: docs
weight: 120
url: /nodejs-net/Aspose.Words/font/engrave/
---

## Font.engrave property

True if the font is formatted as engraved.


```js
get engrave(): boolean
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

