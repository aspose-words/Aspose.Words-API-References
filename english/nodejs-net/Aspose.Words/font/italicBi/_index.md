﻿---
title: Font.italicBi property
linktitle: italicBi property
articleTitle: italicBi property
second_title: Aspose.Words for Node.js
description: "Font.italicBi property. True if the right-to-left text is formatted as italic."
type: docs
weight: 170
url: /nodejs-net/aspose.words/font/italicBi/
---

## Font.italicBi property

True if the right-to-left text is formatted as italic.


```js
get italicBi(): boolean
```

### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Define a set of font settings for left-to-right text.
builder.font.name = "Courier New";
builder.font.size = 16;
builder.font.italic = false;
builder.font.bold = false;
builder.font.localeId = new CultureInfo("en-US", false).LCID;

// Define another set of font settings for right-to-left text.
builder.font.nameBi = "Andalus";
builder.font.sizeBi = 24;
builder.font.italicBi = true;
builder.font.boldBi = true;
builder.font.localeIdBi = new CultureInfo("ar-AR", false).LCID;

// We can use the Bidi flag to indicate whether the text we are about to add
// with the document builder is right-to-left. When we add text with this flag set to true,
// it will be formatted using the right-to-left set of font settings.
builder.font.bidi = true;
builder.write("مرحبًا");

// Set the flag to false, and then add left-to-right text.
// The document builder will format these using the left-to-right set of font settings.
builder.font.bidi = false;
builder.write(" Hello world!");

doc.save(base.artifactsDir + "Font.bidi.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

