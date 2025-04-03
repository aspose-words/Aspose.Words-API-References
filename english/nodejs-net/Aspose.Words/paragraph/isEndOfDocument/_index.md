---
title: Paragraph.isEndOfDocument property
linktitle: isEndOfDocument property
articleTitle: isEndOfDocument property
second_title: Aspose.Words for NodeJs
description: "Paragraph.isEndOfDocument property. True if this paragraph is the last paragraph in the last section of the document."
type: docs
weight: 60
url: /nodejs-net/aspose.words/paragraph/isEndOfDocument/
---

## Paragraph.isEndOfDocument property

True if this paragraph is the last paragraph in the last section of the document.


```js
get isEndOfDocument(): boolean
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
* class [Paragraph](../)

