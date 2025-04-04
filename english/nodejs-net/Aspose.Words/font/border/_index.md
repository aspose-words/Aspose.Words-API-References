---
title: Font.border property
linktitle: border property
articleTitle: border property
second_title: Aspose.Words for Node.js
description: "Font.border property. Returns a [Border](../../border/) object that specifies border for the font."
type: docs
weight: 60
url: /nodejs-net/aspose.words/font/border/
---

## Font.border property

Returns a [Border](../../border/) object that specifies border for the font.



```js
get border(): Aspose.Words.Border
```

### Examples

Shows how to insert a string surrounded by a border into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.border.color = "#008000";
builder.font.border.lineWidth = 2.5;
builder.font.border.lineStyle = aw.LineStyle.DashDotStroker;

builder.write("Text surrounded by green border.");

doc.save(base.artifactsDir + "Border.FontBorder.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

