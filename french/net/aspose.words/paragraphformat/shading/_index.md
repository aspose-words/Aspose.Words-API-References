---
title: ParagraphFormat.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Ombrage de ParagraphFormat pour un style de texte amélioré. Accédez à un objet Ombrage pour rehausser l'attrait visuel de votre paragraphe en toute simplicité.
type: docs
weight: 290
url: /fr/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Renvoie un[`Shading`](../../shading/) objet qui fait référence à la mise en forme de l'ombrage du paragraphe.

```csharp
public Shading Shading { get; }
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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
