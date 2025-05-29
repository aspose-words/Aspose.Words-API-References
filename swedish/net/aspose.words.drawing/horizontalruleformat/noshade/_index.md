---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HorizontalRuleFormat NoShade, styr 3D-skuggning för horisontella linjer. Få en elegant, enfärgad design utan ansträngning!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indikerar förekomsten av 3D-skuggning för den horisontella linjen. Om`sann` , då är den horisontella linjen utan 3D-skuggning och enfärgad används.

```csharp
public bool NoShade { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk`.

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

* class [HorizontalRuleFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
