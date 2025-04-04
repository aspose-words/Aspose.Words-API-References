---
title: ParagraphFormat.outlineLevel property
linktitle: outlineLevel property
articleTitle: outlineLevel property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.outlineLevel property. Specifies the outline level of the paragraph in the document."
type: docs
weight: 260
url: /nodejs-net/aspose.words/paragraphformat/outlineLevel/
---

## ParagraphFormat.outlineLevel property

Specifies the outline level of the paragraph in the document.


```js
get outlineLevel(): Aspose.Words.OutlineLevel
```

### Examples

Shows how to configure paragraph outline levels to create collapsible text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Each paragraph has an OutlineLevel, which could be any number from 1 to 9, or at the default "BodyText" value.
// Setting the property to one of the numbered values will show an arrow to the left
// of the beginning of the paragraph.
builder.paragraphFormat.outlineLevel = aw.OutlineLevel.Level1;
builder.writeln("Paragraph outline level 1.");

// Level 1 is the topmost level. If there is a paragraph with a lower level below a paragraph with a higher level,
// collapsing the higher-level paragraph will collapse the lower level paragraph.
builder.paragraphFormat.outlineLevel = aw.OutlineLevel.Level2;
builder.writeln("Paragraph outline level 2.");

// Two paragraphs of the same level will not collapse each other,
// and the arrows do not collapse the paragraphs they point to.
builder.paragraphFormat.outlineLevel = aw.OutlineLevel.Level3;
builder.writeln("Paragraph outline level 3.");
builder.writeln("Paragraph outline level 3.");

// The default "BodyText" value is the lowest, which a paragraph of any level can collapse.
builder.paragraphFormat.outlineLevel = aw.OutlineLevel.BodyText;
builder.writeln("Paragraph at main text level.");

doc.save(base.artifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

