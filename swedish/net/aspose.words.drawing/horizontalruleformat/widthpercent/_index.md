---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words för .NET
description: HorizontalRuleFormat WidthPercent fast egendom. Hämtar eller ställer in längden på den angivna horisontella regeln uttryckt i procent av fönstrets bredd i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Hämtar eller ställer in längden på den angivna horisontella regeln uttryckt i procent av fönstrets bredd.

```csharp
public double WidthPercent { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kastar när argumentet var utanför intervallet för giltiga värden. |

## Anmärkningar

Giltiga värden sträcker sig från 1 till 100 inklusive.

Standardvärdet är 100.

## Exempel

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
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
