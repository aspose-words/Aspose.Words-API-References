---
title: ParagraphFormat.leftIndent property
linktitle: leftIndent property
articleTitle: leftIndent property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.leftIndent property. Gets or sets the value (in points) that represents the left indent for paragraph."
type: docs
weight: 180
url: /nodejs-net/Aspose.Words/paragraphformat/leftIndent/
---

## ParagraphFormat.leftIndent property

Gets or sets the value (in points) that represents the left indent for paragraph.


```js
get leftIndent(): number
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

