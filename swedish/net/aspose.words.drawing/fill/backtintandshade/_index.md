---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words för .NET
description: Justera egenskapen BackTintAndShade för att enkelt ljusa eller mörka upp bakgrundsfärgen, vilket förbättrar designens visuella attraktionskraft och användarupplevelse.
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Hämtar eller ställer in ett dubbelt värde som ljusar eller mörkar upp bakgrundsfärgen.

```csharp
public double BackTintAndShade { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta om den här egenskapen sätts till ett värde mindre än -1 eller större än 1. |

## Anmärkningar

De tillåtna värdena ligger i intervallet från -1 (mörkast) till 1 (ljusast) för den här egenskapen.

Noll (0) är neutral.

## Exempel

Visar hur man ställer in temafärg för förgrunds-/bakgrundsformfärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Obs: använd inte "BackThemeColor" och "BackTintAndShade" för typsnittsfyllning.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
