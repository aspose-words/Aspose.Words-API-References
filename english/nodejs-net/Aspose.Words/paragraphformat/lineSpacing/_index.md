---
title: ParagraphFormat.lineSpacing property
linktitle: lineSpacing property
articleTitle: lineSpacing property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.lineSpacing property. Gets or sets the line spacing (in points) for the paragraph."
type: docs
weight: 190
url: /nodejs-net/Aspose.Words/paragraphformat/lineSpacing/
---

## ParagraphFormat.lineSpacing property

Gets or sets the line spacing (in points) for the paragraph.


```js
get lineSpacing(): number
```

### Remarks

When [ParagraphFormat.lineSpacingRule](../lineSpacingRule/) property is set to [LineSpacingRule.AtLeast](../../linespacingrule/#AtLeast), the line spacing can be greater than or equal to,
but never less than the specified [ParagraphFormat.lineSpacing](./) value.

When [ParagraphFormat.lineSpacingRule](../lineSpacingRule/) property is set to [LineSpacingRule.Exactly](../../linespacingrule/#Exactly), the line spacing never changes from
the specified [ParagraphFormat.lineSpacing](./) value, even if a larger font is used within the paragraph.




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

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

