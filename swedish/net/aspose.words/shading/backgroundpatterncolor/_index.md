---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Shading BackgroundPatternColor för att anpassa ditt Shading-objekts bakgrundsfärg och förbättra din designs visuella attraktionskraft.
type: docs
weight: 10
url: /sv/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Hämtar eller ställer in färgen som tillämpas på bakgrunden av[`Shading`](../) objekt.

```csharp
public Color BackgroundPatternColor { get; set; }
```

## Exempel

Visar hur man dekorerar text med ramar och skuggning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### Se även

* class [Shading](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
