---
title: Font.underline property
linktitle: underline property
articleTitle: underline property
second_title: Aspose.Words for Node.js
description: "Font.underline property. Gets or sets the type of underline applied to the font."
type: docs
weight: 540
url: /nodejs-net/aspose.words/font/underline/
---

## Font.underline property

Gets or sets the type of underline applied to the font.


```js
get underline(): Aspose.Words.Underline
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

Shows how to insert formatted text using DocumentBuilder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Specify font formatting, then add text.
let font = builder.font;
font.size = 16;
font.bold = true;
font.color = "#0000FF";
font.name = "Courier New";
font.underline = aw.Underline.Dash;

builder.write("Hello world!");
```

Shows how to insert a hyperlink field.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("For more information, please visit the ");

// Insert a hyperlink and emphasize it with custom formatting.
// The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = "#0000FF";
builder.font.underline = aw.Underline.Single;
builder.insertHyperlink("Google website", "https://www.google.com", false);
builder.font.clearFormatting();
builder.writeln(".");

// Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(base.artifactsDir + "DocumentBuilder.insertHyperlink.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

