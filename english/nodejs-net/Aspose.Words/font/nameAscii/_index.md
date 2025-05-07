---
title: Font.nameAscii property
linktitle: nameAscii property
articleTitle: nameAscii property
second_title: Aspose.Words for Node.js
description: "Font.nameAscii property. Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /nodejs-net/aspose.words/font/nameAscii/
---

## Font.nameAscii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).


```js
get nameAscii(): string
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

