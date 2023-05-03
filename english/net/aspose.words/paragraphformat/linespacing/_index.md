---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
second_title: Aspose.Words for .NET API Reference
description: ParagraphFormat LineSpacing property. Gets or sets the line spacing in points for the paragraph in C#.
type: docs
weight: 180
url: /net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Gets or sets the line spacing (in points) for the paragraph.

```csharp
public double LineSpacing { get; set; }
```

## Remarks

When [`LineSpacingRule`](../linespacingrule/) property is set to AtLeast, the line spacing can be greater than or equal to, but never less than the specified `LineSpacing` value.

When [`LineSpacingRule`](../linespacingrule/) property is set to Exactly, the line spacing never changes from the specified `LineSpacing` value, even if a larger font is used within the paragraph.

## Examples

Shows how to work with line spacing.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are three line spacing rules that we can define using the
// paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
// 1 -  Set a minimum amount of spacing.
// This will give vertical padding to lines of text of any size
// that is too small to maintain the minimum line-height.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 -  Set exact spacing.
// Using font sizes that are too large for the spacing will truncate the text.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
// This kind of spacing will scale to different font sizes.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../paragraphformat/)
* assembly [Aspose.Words](../../../)
