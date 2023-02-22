---
title: Shading.ForegroundPatternColor
second_title: Référence de l'API Aspose.Words pour .NET
description: Shading propriété. Obtient ou définit la couleur appliquée au premier plan de lobjet Shading.
type: docs
weight: 20
url: /fr/net/aspose.words/shading/foregroundpatterncolor/
---
## Shading.ForegroundPatternColor property

Obtient ou définit la couleur appliquée au premier plan de l'objet Shading.

```csharp
public Color ForegroundPatternColor { get; set; }
```

### Exemples

Montre comment décorer du texte avec des bordures et des ombres.

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

### Voir également

* class [Shading](../)
* espace de noms [Aspose.Words](../../shading/)
* Assemblée [Aspose.Words](../../../)


