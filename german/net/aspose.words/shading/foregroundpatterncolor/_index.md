---
title: Shading.ForegroundPatternColor
linktitle: ForegroundPatternColor
articleTitle: ForegroundPatternColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Shading ForegroundPatternColor-Eigenschaft, um die Vordergrundfarbe Ihres Shading-Objekts für ein verbessertes Design und eine bessere Optik anzupassen.
type: docs
weight: 40
url: /de/net/aspose.words/shading/foregroundpatterncolor/
---
## Shading.ForegroundPatternColor property

Ruft die Farbe ab oder legt sie fest, die auf den Vordergrund des[`Shading`](../) Objekt.

```csharp
public Color ForegroundPatternColor { get; set; }
```

## Beispiele

Zeigt, wie Sie Text mit Rahmen und Schattierungen verzieren.

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
