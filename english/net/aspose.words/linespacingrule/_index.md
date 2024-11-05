---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words for .NET
description: Aspose.Words.LineSpacingRule enum. Specifies line spacing values for a paragraph in C#.
type: docs
weight: 3820
url: /net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Specifies line spacing values for a paragraph.

```csharp
public enum LineSpacingRule
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AtLeast | `0` | The line spacing can be greater than or equal to, but never less than, the value specified in the [`LineSpacing`](../paragraphformat/linespacing/) property. |
| Exactly | `1` | The line spacing never changes from the value specified in the [`LineSpacing`](../paragraphformat/linespacing/) property, even if a larger font is used within the paragraph. |
| Multiple | `2` | The line spacing is specified in the [`LineSpacing`](../paragraphformat/linespacing/) property as the number of lines. One line equals 12 points. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
