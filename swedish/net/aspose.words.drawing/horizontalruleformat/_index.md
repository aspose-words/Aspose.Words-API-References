---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.HorizontalRuleFormat för avancerad formatering av horisontella linjer. Förbättra din dokumentdesign utan ansträngning!
type: docs
weight: 1380
url: /sv/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Representerar formatering av horisontell linje.

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public class HorizontalRuleFormat
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Hämtar eller ställer in justeringen av den horisontella linjen. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Hämtar eller ställer in penselfärgen som fyller den horisontella linjen. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Hämtar eller ställer in höjden på den horisontella linjen. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Indikerar förekomsten av 3D-skuggning för den horisontella linjen. Om`sann` , då är den horisontella linjen utan 3D-skuggning och enfärgad används. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Hämtar eller ställer in längden på den angivna horisontella linjen uttryckt som en procentandel av fönsterbredden. |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
