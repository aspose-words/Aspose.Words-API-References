---
title: HorizontalRuleFormat.Height
second_title: Aspose.Words for .NET API Reference
description: HorizontalRuleFormat property. Gets or sets the height of the horizontal rule in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Gets or sets the height of the horizontal rule.

```csharp
public double Height { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throws when argument was out of the range of valid values. |

## Remarks

This is a shortcut to the [`Height`](../../shapebase/height/) property.

Valid values ​​range from 0 to 1584 inclusive.

The default value is 1.5.

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
* namespace [Aspose.Words.Drawing](../../horizontalruleformat/)
* assembly [Aspose.Words](../../../)
