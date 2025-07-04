---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words for .NET
description: Discover the HorizontalRuleFormat WidthPercent property to easily customize your horizontal rule's length as a percentage of window width for better design control.
type: docs
weight: 50
url: /net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width.

```csharp
public double WidthPercent { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throws when argument was out of the range of valid values. |

## Remarks

Valid values ​​range from 1 to 100 inclusive.

The default value is 100.

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

Assert.That(shape.IsHorizontalRule, Is.True);
Assert.That(shape.HorizontalRuleFormat.NoShade, Is.True);
```

### See Also

* class [HorizontalRuleFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
