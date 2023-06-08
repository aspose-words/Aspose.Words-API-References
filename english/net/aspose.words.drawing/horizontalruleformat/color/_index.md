---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: HorizontalRuleFormat Color property. Gets or sets the brush color that fills the horizontal rule in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Gets or sets the brush color that fills the horizontal rule.

```csharp
public Color Color { get; set; }
```

## Remarks

This is a shortcut to the [`Color`](../../fill/color/) property.

The default value is Gray.

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

* class [HorizontalRuleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
