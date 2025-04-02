---
title: Font.bold property
linktitle: bold property
articleTitle: bold property
second_title: Aspose.Words for NodeJs
description: "Font.bold property. True if the font is formatted as bold."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/font/bold/
---

## Font.bold property

True if the font is formatted as bold.


```js
get bold(): boolean
```

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

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

