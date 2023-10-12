---
title: Shape.HorizontalRuleFormat
second_title: Aspose.Words för .NET API Referens
description: Shape fast egendom. Ger tillgång till egenskaperna för den horisontella regelformen. För en form som inte är en horisontell regel returnerarnull .
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Ger tillgång till egenskaperna för den horisontella regelformen. För en form som inte är en horisontell regel, returnerar`null` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

### Exempel

Visar hur man infogar en horisontell regelform och anpassar dess formatering.

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
* namnutrymme [Aspose.Words.Drawing](../../shape/)
* hopsättning [Aspose.Words](../../../)


