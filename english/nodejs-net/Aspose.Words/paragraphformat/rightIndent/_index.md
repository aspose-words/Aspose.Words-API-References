---
title: ParagraphFormat.rightIndent property
linktitle: rightIndent property
articleTitle: rightIndent property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.rightIndent property. Gets or sets the value (in points) that represents the right indent for paragraph."
type: docs
weight: 280
url: /nodejs-net/aspose.words/paragraphformat/rightIndent/
---

## ParagraphFormat.rightIndent property

Gets or sets the value (in points) that represents the right indent for paragraph.


```js
get rightIndent(): number
```

### Examples

Shows how to configure paragraph formatting to create off-center text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Center all text that the document builder writes, and set up indents.
// The indent configuration below will create a body of text that will sit asymmetrically on the page.
// The "center" that we align the text to will be the middle of the body of text, not the middle of the page.
let paragraphFormat = builder.paragraphFormat;
paragraphFormat.alignment = aw.ParagraphAlignment.Center;
paragraphFormat.leftIndent = 100;
paragraphFormat.rightIndent = 50;
paragraphFormat.spaceAfter = 25;

builder.writeln(
  "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.writeln(
  "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.save(base.artifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

