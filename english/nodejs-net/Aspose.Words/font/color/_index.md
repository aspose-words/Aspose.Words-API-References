---
title: Font.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Node.js
description: "Font.color property. Gets or sets the color of the font."
type: docs
weight: 70
url: /nodejs-net/aspose.words/font/color/
---

## Font.color property

Gets or sets the color of the font.


```js
get color(): string
```

### Examples

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

