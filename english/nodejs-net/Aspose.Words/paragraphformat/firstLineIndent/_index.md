---
title: ParagraphFormat.firstLineIndent property
linktitle: firstLineIndent property
articleTitle: firstLineIndent property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.firstLineIndent property. Gets or sets the value (in points) for a first line or hanging indent"
type: docs
weight: 120
url: /nodejs-net/aspose.words/paragraphformat/firstLineIndent/
---

## ParagraphFormat.firstLineIndent property

Gets or sets the value (in points) for a first line or hanging indent.
Use positive values to set the first-line indent, and negative values to set the hanging indent.




```js
get firstLineIndent(): number
```

### Examples

Shows how to insert a paragraph into the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let font = builder.font;
font.size = 16;
font.bold = true;
font.color = "#0000FF";
font.name = "Arial";
font.underline = aw.Underline.Dash;

let paragraphFormat = builder.paragraphFormat;
paragraphFormat.firstLineIndent = 8;
paragraphFormat.alignment = aw.ParagraphAlignment.Justify;
paragraphFormat.addSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.addSpaceBetweenFarEastAndDigit = true;
paragraphFormat.keepTogether = true;

// The "Writeln" method ends the paragraph after appending text
// and then starts a new line, adding a new paragraph.
builder.writeln("Hello world!");

expect(builder.currentParagraph.isEndOfDocument).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

