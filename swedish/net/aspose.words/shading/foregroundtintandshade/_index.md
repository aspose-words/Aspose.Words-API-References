---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words för .NET
description: Justera egenskapen ForegroundTintAndShade för att enkelt ljusa eller mörka upp dina temafärger, vilket förbättrar designens visuella attraktionskraft.
type: docs
weight: 60
url: /sv/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Hämtar eller ställer in ett dubbelvärde som ljusar eller mörkar upp en förgrundstemafärg.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Kasta om den här egenskapen sätts till ett värde mindre än -1 eller större än 1. |
| InvalidOperationException | Utlös om den här egenskapen anges för skuggningsobjekt med icke-temafärger. |

## Anmärkningar

De tillåtna värdena ligger i intervallet från -1 (mörkast) till 1 (ljusast) för den här egenskapen.

Noll (0) är neutral.

## Exempel

Visar hur man ställer in förgrunds- och bakgrundsfärger för skuggningstextur.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Se även

* class [Shading](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
