---
title: Shading.BackgroundPatternColor
second_title: Aspose.Words für .NET-API-Referenz
description: Shading eigendom. Ruft die Farbe ab die auf den Hintergrund des angewendet wird oder legt diese festShading Objekt.
type: docs
weight: 10
url: /de/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Ruft die Farbe ab, die auf den Hintergrund des angewendet wird, oder legt diese fest[`Shading`](../) Objekt.

```csharp
public Color BackgroundPatternColor { get; set; }
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

* class [Shading](../)
* namensraum [Aspose.Words](../../shading/)
* Montage [Aspose.Words](../../../)


