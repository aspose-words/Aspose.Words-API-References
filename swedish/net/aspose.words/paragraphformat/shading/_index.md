---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat Shading för förbättrad textformatering. Få tillgång till ett skuggningsobjekt för att enkelt höja styckets visuella attraktionskraft.
type: docs
weight: 290
url: /sv/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Returnerar en[`Shading`](../../shading/) objekt som refererar till skuggningsformateringen för stycket.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
