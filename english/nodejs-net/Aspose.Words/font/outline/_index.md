---
title: Font.outline property
linktitle: outline property
articleTitle: outline property
second_title: Aspose.Words for NodeJs
description: "Font.outline property. True if the font is formatted as outline."
type: docs
weight: 300
url: /nodejs-net/aspose.words/font/outline/
---

## Font.outline property

True if the font is formatted as outline.


```js
get outline(): boolean
```

### Examples

Shows how to create a run of text formatted as outline.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Set the Outline flag to change the text's fill color to white and
// leave a thin outline around each character in the original color of the text. 
builder.font.outline = true;
builder.font.color = "#0000FF";
builder.font.size = 36;

builder.writeln("This text has an outline.");

doc.save(base.artifactsDir + "Font.outline.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

