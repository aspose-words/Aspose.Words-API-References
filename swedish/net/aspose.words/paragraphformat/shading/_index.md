---
title: ParagraphFormat.Shading
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Returnerar ett Shadingobjekt som refererar till skuggformateringen för stycket.
type: docs
weight: 270
url: /sv/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Returnerar ett Shading-objekt som refererar till skuggformateringen för stycket.

```csharp
public Shading Shading { get; }
```

### Exempel

Visar hur man dekorerar text med kanter och skuggningar.

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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


