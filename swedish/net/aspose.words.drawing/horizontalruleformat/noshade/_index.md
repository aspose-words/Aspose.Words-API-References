---
title: HorizontalRuleFormat.NoShade
second_title: Aspose.Words för .NET API Referens
description: HorizontalRuleFormat fast egendom. Indikerar närvaron av 3Dskuggning för den horisontella regeln. Om sant är den horisontella regeln utan 3Dskuggning och solid färg används.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indikerar närvaron av 3D-skuggning för den horisontella regeln. Om sant är den horisontella regeln utan 3D-skuggning och solid färg används.

```csharp
public bool NoShade { get; set; }
```

### Anmärkningar

Standardvärdet är falskt.

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

* class [HorizontalRuleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../horizontalruleformat/)
* hopsättning [Aspose.Words](../../../)


