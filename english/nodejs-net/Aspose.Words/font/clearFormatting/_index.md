---
title: Font.clearFormatting method
linktitle: clearFormatting method
articleTitle: clearFormatting method
second_title: Aspose.Words for Node.js
description: "Font.clearFormatting method. Resets to default font formatting."
type: docs
weight: 560
url: /nodejs-net/aspose.words/font/clearFormatting/
---

## clearFormatting() {#default}

Resets to default font formatting.


```js
clearFormatting()
```

### Remarks

Removes all font formatting specified explicitly on the object from which
[Font](../) was obtained so the font formatting will be inherited from
the appropriate parent.




### Examples

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

