---
title: Font.underlineColor property
linktitle: underlineColor property
articleTitle: underlineColor property
second_title: Aspose.Words for NodeJs
description: "Font.underlineColor property. Gets or sets the color of the underline applied to the font."
type: docs
weight: 550
url: /nodejs-net/aspose.words/font/underlineColor/
---

## Font.underlineColor property

Gets or sets the color of the underline applied to the font.


```js
get underlineColor(): string
```

### Examples

Shows how to configure the style and color of a text underline.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.underline = aw.Underline.Dotted;
builder.font.underlineColor = "#FF0000";

builder.writeln("Underlined text.");

doc.save(base.artifactsDir + "Font.Underlines.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

