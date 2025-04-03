---
title: Paragraph.breakIsStyleSeparator property
linktitle: breakIsStyleSeparator property
articleTitle: breakIsStyleSeparator property
second_title: Aspose.Words for NodeJs
description: "Paragraph.breakIsStyleSeparator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /nodejs-net/aspose.words/paragraph/breakIsStyleSeparator/
---

## Paragraph.breakIsStyleSeparator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```js
get breakIsStyleSeparator(): boolean
```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertTableOfContents("\\o \\h \\z \\u");
builder.insertBreak(aw.BreakType.PageBreak);

// Insert a paragraph with a style that the TOC will pick up as an entry.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;

// Both these strings are in the same paragraph and will therefore show up on the same TOC entry.
builder.write("Heading 1. ");
builder.write("Will appear in the TOC. ");

// If we insert a style separator, we can write more text in the same paragraph
// and use a different style without showing up in the TOC.
// If we use a heading type style after the separator, we can draw multiple TOC entries from one document text line.
builder.insertStyleSeparator();
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Quote;
builder.write("Won't appear in the TOC. ");

expect(doc.firstSection.body.firstParagraph.breakIsStyleSeparator).toEqual(true);

doc.updateFields();
doc.save(base.artifactsDir + "Paragraph.breakIsStyleSeparator.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

