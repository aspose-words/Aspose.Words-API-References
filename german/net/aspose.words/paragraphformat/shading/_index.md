---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words für .NET
description: Entdecken Sie die ParagraphFormat-Schattierungseigenschaft für verbesserte Textgestaltung. Greifen Sie auf ein Schattierungsobjekt zu, um die visuelle Attraktivität Ihres Absatzes mühelos zu steigern.
type: docs
weight: 290
url: /de/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Gibt einen[`Shading`](../../shading/) Objekt, das sich auf die Schattierungsformatierung für den Absatz bezieht.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
