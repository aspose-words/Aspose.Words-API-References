---
title: Font.italic property
linktitle: italic property
articleTitle: italic property
second_title: Aspose.Words for NodeJs
description: "Font.italic property. True if the font is formatted as italic."
type: docs
weight: 160
url: /nodejs-net/aspose.words/font/italic/
---

## Font.italic property

True if the font is formatted as italic.


```js
get italic(): boolean
```

### Examples

Shows how to write italicized text using a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.size = 36;
builder.font.italic = true;
builder.writeln("Hello world!");

doc.save(base.artifactsDir + "Font.italic.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

