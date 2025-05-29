---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words för .NET
description: Justera höjden på din horisontella linje enkelt. Utforska egenskapen Höjd för anpassningsbar design i dina webbprojekt. Förbättra din layout idag!
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Hämtar eller ställer in höjden på den horisontella linjen.

```csharp
public double Height { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta ett värde när argumentet låg utanför intervallet för giltiga värden. |

## Anmärkningar

Detta är en genväg till[`Height`](../../shapebase/height/) egendom.

Giltiga värden sträcker sig från 0 till 1584.

Standardvärdet är 1,5.

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
