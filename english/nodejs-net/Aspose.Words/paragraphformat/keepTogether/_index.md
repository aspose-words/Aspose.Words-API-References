---
title: ParagraphFormat.keepTogether property
linktitle: keepTogether property
articleTitle: keepTogether property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.keepTogether property. True if all lines in the paragraph are to remain on the same page."
type: docs
weight: 160
url: /nodejs-net/aspose.words/paragraphformat/keepTogether/
---

## ParagraphFormat.keepTogether property

True if all lines in the paragraph are to remain on the same page.


```js
get keepTogether(): boolean
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

