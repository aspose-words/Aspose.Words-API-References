---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.HorizontalRuleAlignment enum. Represents the alignment for the specified horizontal rule in C#.
type: docs
weight: 1350
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

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
