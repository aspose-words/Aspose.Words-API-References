---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words per .NET
description: Shading Texture proprietà. Ottiene o imposta la texture dellombreggiatura in C#.
type: docs
weight: 70
url: /it/net/aspose.words/shading/texture/
---
## Shading.Texture property

Ottiene o imposta la texture dell'ombreggiatura.

```csharp
public TextureIndex Texture { get; set; }
```

## Esempi

Mostra come decorare il testo con bordi e ombreggiature.

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

### Guarda anche

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
