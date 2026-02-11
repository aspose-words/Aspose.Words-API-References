---
title: LineSpacingRule enumeration
linktitle: LineSpacingRule enumeration
articleTitle: LineSpacingRule enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.LineSpacingRule enumeration. Specifies line spacing values for a paragraph."
type: docs
weight: 790
url: /nodejs-net/aspose.words/linespacingrule/
---

## LineSpacingRule enumeration

Specifies line spacing values for a paragraph.


### Members

| Name | Description |
| --- | --- |
| AtLeast | The line spacing can be greater than or equal to, but never less than, the value specified in the [ParagraphFormat.lineSpacing](../paragraphformat/lineSpacing/) property. |
| Exactly | The line spacing never changes from the value specified in the [ParagraphFormat.lineSpacing](../paragraphformat/lineSpacing/) property, even if a larger font is used within the paragraph. |
| Multiple | The line spacing is specified in the [ParagraphFormat.lineSpacing](../paragraphformat/lineSpacing/) property as the number of lines. One line equals 12 points. |

### Examples

Shows how to work with line spacing.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are three line spacing rules that we can define using the
// paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
// 1 -  Set a minimum amount of spacing.
// This will give vertical padding to lines of text of any size
// that is too small to maintain the minimum line-height.
builder.paragraphFormat.lineSpacingRule = aw.LineSpacingRule.AtLeast;
builder.paragraphFormat.lineSpacing = 20;

builder.writeln("Minimum line spacing of 20.");
builder.writeln("Minimum line spacing of 20.");

// 2 -  Set exact spacing.
// Using font sizes that are too large for the spacing will truncate the text.
builder.paragraphFormat.lineSpacingRule = aw.LineSpacingRule.Exactly;
builder.paragraphFormat.lineSpacing = 5;

builder.writeln("Line spacing of exactly 5.");
builder.writeln("Line spacing of exactly 5.");

// 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
// This kind of spacing will scale to different font sizes.
builder.paragraphFormat.lineSpacingRule = aw.LineSpacingRule.Multiple;
builder.paragraphFormat.lineSpacing = 18;

builder.writeln("Line spacing of 1.5 default lines.");
builder.writeln("Line spacing of 1.5 default lines.");

doc.save(base.artifactsDir + "ParagraphFormat.lineSpacing.docx");
```

### See Also

* module [Aspose.Words](../)

