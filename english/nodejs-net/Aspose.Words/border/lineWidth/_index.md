---
title: Border.lineWidth property
linktitle: lineWidth property
articleTitle: lineWidth property
second_title: Aspose.Words for NodeJs
description: "Border.lineWidth property. Gets or sets the border width in points."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/border/lineWidth/
---

## Border.lineWidth property

Gets or sets the border width in points.


```js
get lineWidth(): number
```

### Remarks

If you set line width greater than zero when line style is none, the line style is
automatically changed to single line.




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

