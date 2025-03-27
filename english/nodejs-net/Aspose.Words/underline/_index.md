---
title: Underline enumeration
linktitle: Underline enumeration
articleTitle: Underline enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Underline enumeration. Indicates type of the underline applied to a font."
type: docs
weight: 1440
url: /nodejs-net/Aspose.Words/underline/
---

## Underline enumeration

Indicates type of the underline applied to a font.


### Members

| Name | Description |
| --- | --- |
| None |  |
| Single |  |
| Words |  |
| Double |  |
| Dotted |  |
| Thick |  |
| Dash |  |
| DashLong |  |
| DotDash |  |
| DotDotDash |  |
| Wavy |  |
| DottedHeavy |  |
| DashHeavy |  |
| DashLongHeavy |  |
| DotDashHeavy |  |
| DotDotDashHeavy |  |
| WavyHeavy |  |
| WavyDouble |  |

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

* module [Aspose.Words](../)

