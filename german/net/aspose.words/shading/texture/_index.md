---
title: Shading.Texture
second_title: Aspose.Words für .NET-API-Referenz
description: Shading eigendom. Ruft die Schattierungstextur ab oder legt sie fest.
type: docs
weight: 70
url: /de/net/aspose.words/shading/texture/
---
## Shading.Texture property

Ruft die Schattierungstextur ab oder legt sie fest.

```csharp
public TextureIndex Texture { get; set; }
```

### Beispiele

Zeigt, wie Text mit Rändern und Schattierungen dekoriert wird.

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

### Siehe auch

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* namensraum [Aspose.Words](../../shading/)
* Montage [Aspose.Words](../../../)


