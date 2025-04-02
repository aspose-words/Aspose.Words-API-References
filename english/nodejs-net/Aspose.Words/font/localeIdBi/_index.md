---
title: Font.localeIdBi property
linktitle: localeIdBi property
articleTitle: localeIdBi property
second_title: Aspose.Words for NodeJs
description: "Font.localeIdBi property. Gets or sets the locale identifier (language) of the formatted right-to-left characters."
type: docs
weight: 210
url: /nodejs-net/Aspose.Words/font/localeIdBi/
---

## Font.localeIdBi property

Gets or sets the locale identifier (language) of the formatted right-to-left characters.


```js
get localeIdBi(): number
```

### Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


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

