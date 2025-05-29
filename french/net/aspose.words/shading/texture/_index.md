---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Texture d'ombrage pour sublimer vos créations. Personnalisez et définissez facilement des textures pour des effets visuels époustouflants dans vos projets.
type: docs
weight: 70
url: /fr/net/aspose.words/shading/texture/
---
## Shading.Texture property

Obtient ou définit la texture d'ombrage.

```csharp
public TextureIndex Texture { get; set; }
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

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
