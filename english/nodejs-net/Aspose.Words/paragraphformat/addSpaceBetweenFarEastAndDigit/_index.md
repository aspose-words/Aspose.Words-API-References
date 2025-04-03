---
title: ParagraphFormat.addSpaceBetweenFarEastAndDigit property
linktitle: addSpaceBetweenFarEastAndDigit property
articleTitle: addSpaceBetweenFarEastAndDigit property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.addSpaceBetweenFarEastAndDigit property. Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph."
type: docs
weight: 20
url: /nodejs-net/aspose.words/paragraphformat/addSpaceBetweenFarEastAndDigit/
---

## ParagraphFormat.addSpaceBetweenFarEastAndDigit property

Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions
of numbers and regions of East Asian text in the current paragraph.


```js
get addSpaceBetweenFarEastAndDigit(): boolean
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

