---
title: Color
second_title: Aspose.Words for .NET API Reference
description: Gets or sets the brush color that fills the horizontal rule.
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

This is a shortcut to the Color property.

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

* class [HorizontalRuleFormat](../../horizontalruleformat)
* namespace [Aspose.Words.Drawing](../../horizontalruleformat)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
