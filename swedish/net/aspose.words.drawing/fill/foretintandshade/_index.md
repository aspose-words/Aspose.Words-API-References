---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words för .NET
description: Justera egenskapen ForeTintAndShade för att enkelt ljusa upp eller mörka upp förgrundsfärgen, vilket förbättrar din design med precision och kreativitet.
type: docs
weight: 90
url: /sv/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar förgrundsfärgen.

```csharp
public double ForeTintAndShade { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta om den här egenskapen sätts till ett värde mindre än -1 eller större än 1. |

## Anmärkningar

De tillåtna värdena ligger i intervallet från -1 (mörkast) till 1 (ljusast) för den här egenskapen.

Noll (0) är neutral.

## Exempel

Visar hur man hanterar ljusare och mörkare förgrundsteckensnittsfärg.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
