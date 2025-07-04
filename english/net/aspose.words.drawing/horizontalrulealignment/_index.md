---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.HorizontalRuleAlignment enum for precise control over horizontal rule alignment, enhancing your document formatting and design.
type: docs
weight: 1360
url: /net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

Represents the alignment for the specified horizontal rule.

```csharp
public enum HorizontalRuleAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | `0` | Aligned to the left. |
| Center | `1` | Aligned to the center. |
| Right | `2` | Aligned to the right. |

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
