---
title: Shading.BackgroundPatternColor
linktitle: BackgroundPatternColor
articleTitle: BackgroundPatternColor
second_title: Aspose.Words pour .NET
description: Shading BackgroundPatternColor propriété. Obtient ou définit la couleur appliquée à larrièreplan duShading objet en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Obtient ou définit la couleur appliquée à l'arrière-plan du[`Shading`](../) objet.

```csharp
public Color BackgroundPatternColor { get; set; }
```

## Exemples

Montre comment décorer du texte avec des bordures et des ombrages.

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
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
