---
title: Font.nameOther property
linktitle: nameOther property
articleTitle: nameOther property
second_title: Aspose.Words for NodeJs
description: "Font.nameOther property. Returns or sets the font used for characters with character codes from 128 through 255."
type: docs
weight: 270
url: /nodejs-net/aspose.words/font/nameOther/
---

## Font.nameOther property

Returns or sets the font used for characters with character codes from 128 through 255.


```js
get nameOther(): string
```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Suppose a run that we use the builder to insert while using this font configuration
// contains characters within the ASCII characters' range. In that case,
// it will display those characters using this font.
builder.font.nameAscii = "Calibri";

// With no other font specified, the builder will also apply this font to all characters that it inserts.
expect(builder.font.name).toEqual("Calibri");

// Specify a font to use for all characters outside of the ASCII range.
// Ideally, this font should have a glyph for each required non-ASCII character code.
builder.font.nameOther = "Courier New";

// Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
// Each character will be displayed using either of the fonts, depending on.
builder.writeln("Hello, Привет");

doc.save(base.artifactsDir + "Font.nameAscii.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)
* property [Font.name](../name/)

