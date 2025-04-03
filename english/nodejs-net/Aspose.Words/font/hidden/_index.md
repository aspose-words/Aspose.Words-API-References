---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for NodeJs
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /nodejs-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


```js
get hidden(): boolean
```

### Examples

Shows how to create a run of hidden text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// With the Hidden flag set to true, any text that we create using this Font object will be invisible in the document.
// We will not see or highlight hidden text unless we enable the "Hidden text" option
// found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
// and we will be able to access this text programmatically.
// It is not advised to use this method to hide sensitive information.
builder.font.hidden = true;
builder.font.size = 36;

builder.writeln("This text will not be visible in the document.");

doc.save(base.artifactsDir + "Font.hidden.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

