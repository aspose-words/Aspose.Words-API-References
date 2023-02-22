---
title: HorizontalRuleFormat.Alignment
second_title: Aspose.Words för .NET API Referens
description: HorizontalRuleFormat fast egendom. Hämtar eller ställer in justeringen av den horisontella regeln.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Hämtar eller ställer in justeringen av den horisontella regeln.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

### Anmärkningar

Standardvärdet ärLeft.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../horizontalruleformat/)
* hopsättning [Aspose.Words](../../../)


