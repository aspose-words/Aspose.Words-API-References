---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words för .NET
description: Få åtkomst till och anpassa egenskaperna för HorizontalRuleFormat för ökad designflexibilitet. Optimera dina former med skräddarsydda inställningar för unika resultat.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Ger åtkomst till egenskaperna för den horisontella regelformen. För en form som inte är en horisontell regel returneras`null` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

## Exempel

Visar hur man infogar en horisontell linjeform och anpassar dess formatering.

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

### Se även

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
