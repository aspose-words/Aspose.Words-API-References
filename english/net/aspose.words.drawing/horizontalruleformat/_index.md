---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.HorizontalRuleFormat class. Represents horizontal rule formatting in C#.
type: docs
weight: 1220
url: /net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Represents horizontal rule formatting.

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public class HorizontalRuleFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Gets or sets the alignment of the horizontal rule. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Gets or sets the brush color that fills the horizontal rule. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Gets or sets the height of the horizontal rule. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Indicates the presence of 3D shading for the horizontal rule. If `true`, then the horizontal rule is without 3D shading and solid color is used. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width. |

## Examples

Shows how to insert a horizontal rule shape, and customize its formatting.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
