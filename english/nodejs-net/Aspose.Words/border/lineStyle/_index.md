---
title: Border.lineStyle property
linktitle: lineStyle property
articleTitle: lineStyle property
second_title: Aspose.Words for Node.js
description: "Border.lineStyle property. Gets or sets the border style."
type: docs
weight: 40
url: /nodejs-net/aspose.words/border/lineStyle/
---

## Border.lineStyle property

Gets or sets the border style.


```js
get lineStyle(): Aspose.Words.LineStyle
```

### Remarks

If you set line style to none, then line width is automatically changed to zero.




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
* class [Border](../)

