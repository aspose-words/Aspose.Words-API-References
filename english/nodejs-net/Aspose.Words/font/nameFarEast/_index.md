---
title: Font.nameFarEast property
linktitle: nameFarEast property
articleTitle: nameFarEast property
second_title: Aspose.Words for Node.js
description: "Font.nameFarEast property. Returns or sets an East Asian font name."
type: docs
weight: 260
url: /nodejs-net/aspose.words/font/nameFarEast/
---

## Font.nameFarEast property

Returns or sets an East Asian font name.


```js
get nameFarEast(): string
```

### Examples

Shows how to insert and format text in a Far East language.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Specify font settings that the document builder will apply to any text that it inserts.
builder.font.name = "Courier New";
builder.font.localeId = new CultureInfo("en-US", false).LCID;

// Name "FarEast" equivalents for our font and locale.
// If the builder inserts Asian characters with this Font configuration, then each run that contains
// these characters will display them using the "FarEast" font/locale instead of the default.
// This could be useful when a western font does not have ideal representations for Asian characters.
builder.font.nameFarEast = "SimSun";
builder.font.localeIdFarEast = new CultureInfo("zh-CN", false).LCID;

// This text will be displayed in the default font/locale.
builder.writeln("Hello world!");

// Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
builder.writeln("你好世界");

doc.save(base.artifactsDir + "Font.farEast.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)
* property [Font.name](../name/)

