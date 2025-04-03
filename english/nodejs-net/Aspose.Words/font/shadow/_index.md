---
title: Font.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for NodeJs
description: "Font.shadow property. True if the font is formatted as shadowed."
type: docs
weight: 340
url: /nodejs-net/aspose.words/font/shadow/
---

## Font.shadow property

True if the font is formatted as shadowed.


```js
get shadow(): boolean
```

### Examples

Shows how to create a run of text formatted with a shadow.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Set the Shadow flag to apply an offset shadow effect,
// making it look like the letters are floating above the page.
builder.font.shadow = true;
builder.font.size = 36;

builder.writeln("This text has a shadow.");

doc.save(base.artifactsDir + "Font.shadow.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

