---
title: Border.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for NodeJs
description: "Border.color property. Gets or sets the border color."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/border/color/
---

## Border.color property

Gets or sets the border color.


```js
get color(): string
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
* class [Border](../)

