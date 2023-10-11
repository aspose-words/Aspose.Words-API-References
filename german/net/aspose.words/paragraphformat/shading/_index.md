---
title: ParagraphFormat.Shading
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Gibt a zurückShading Objekt das sich auf die Schattierungsformatierung für den Absatz bezieht.
type: docs
weight: 280
url: /de/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Gibt a zurück[`Shading`](../../shading/) Objekt, das sich auf die Schattierungsformatierung für den Absatz bezieht.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


