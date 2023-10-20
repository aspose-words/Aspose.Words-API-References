---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words för .NET
description: Font Shading fast egendom. Returnerar enShading objekt som hänvisar till skuggformateringen för teckensnittet i C#.
type: docs
weight: 320
url: /sv/net/aspose.words/font/shading/
---
## Font.Shading property

Returnerar en[`Shading`](../../shading/) objekt som hänvisar till skuggformateringen för teckensnittet.

```csharp
public Shading Shading { get; }
```

## Exempel

Visar hur man tillämpar skuggning på text som skapats av en dokumentbyggare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Ett sätt att göra texten som skapats med vår vita teckenfärg synlig
// är att tillämpa en bakgrundsskuggningseffekt.
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
