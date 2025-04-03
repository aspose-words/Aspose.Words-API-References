---
title: Font.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for NodeJs
description: "Font.bidi property. Specifies whether the contents of this run shall have right-to-left characteristics."
type: docs
weight: 30
url: /nodejs-net/aspose.words/font/bidi/
---

## Font.bidi property

Specifies whether the contents of this run shall have right-to-left characteristics.


```js
get bidi(): boolean
```

### Remarks

This property, when on, shall not be used with strongly left-to-right text. Any behavior under that condition is unspecified.
This property, when off, shall not be used with strong right-to-left text. Any behavior under that condition is unspecified.

When the contents of this run are displayed, all characters shall be treated as complex script characters for formatting
purposes. This means that [Font.boldBi](../boldBi/), [Font.italicBi](../italicBi/), [Font.sizeBi](../sizeBi/) and a corresponding font name
will be used when rendering this run.

Also, when the contents of this run are displayed, this property acts as a right-to-left override for characters
which are classified as "weak types" and "neutral types".




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

