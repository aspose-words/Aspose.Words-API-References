---
title: DocumentBuilder.InsertHorizontalRule
linktitle: InsertHorizontalRule
articleTitle: InsertHorizontalRule
second_title: Aspose.Words for .NET
description: Enhance your documents with the DocumentBuilder InsertHorizontalRule method, effortlessly adding stylish horizontal lines for better organization and visual appeal.
type: docs
weight: 370
url: /net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

Inserts a horizontal rule shape into the document.

```csharp
public Shape InsertHorizontalRule()
```

### Return Value

The shape that is a horizontal rule.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
