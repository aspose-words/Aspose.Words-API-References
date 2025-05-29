---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font Shading, som tillhandahåller ett skuggningsobjekt för anpassningsbar teckensnittsformatering, vilket förbättrar textens visuella attraktionskraft.
type: docs
weight: 330
url: /sv/net/aspose.words/font/shading/
---
## Font.Shading property

Returnerar en[`Shading`](../../shading/) objekt som refererar till skuggningsformateringen för teckensnittet.

```csharp
public Shading Shading { get; }
```

## Exempel

Visar hur man använder skuggning på text som skapats av en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Ett sätt att göra texten som skapats med vår vita typsnittsfärg synlig
// är att applicera en bakgrundsskuggningseffekt.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Se även

* class [Shading](../../shading/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
