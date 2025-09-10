---
title: OutlineLevel enumeration
linktitle: OutlineLevel enumeration
articleTitle: OutlineLevel enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.OutlineLevel enumeration. Specifies the outline level of a paragraph in the document."
type: docs
weight: 930
url: /nodejs-net/aspose.words/outlinelevel/
---

## OutlineLevel enumeration

Specifies the outline level of a paragraph in the document.


### Members

| Name | Description |
| --- | --- |
| Level1 | The paragraph is at the outline level 1 (topmost level). |
| Level2 | The paragraph is at the outline level 2. |
| Level3 | The paragraph is at the outline level 3. |
| Level4 | The paragraph is at the outline level 4. |
| Level5 | The paragraph is at the outline level 5. |
| Level6 | The paragraph is at the outline level 6. |
| Level7 | The paragraph is at the outline level 7. |
| Level8 | The paragraph is at the outline level 8. |
| Level9 | The paragraph is at the outline level 9. |
| BodyText | The paragraph is at the level of the main text. |

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

* module [Aspose.Words](../)

