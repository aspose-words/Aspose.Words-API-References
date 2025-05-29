---
title: GraphicsQualityOptions.CompositingQuality
linktitle: CompositingQuality
articleTitle: CompositingQuality
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CompositingQuality de GraphicsQualityOptions pour améliorer le rendu de vos images. Optimisez vos images composées pour une qualité visuelle exceptionnelle !
type: docs
weight: 30
url: /fr/net/aspose.words.saving/graphicsqualityoptions/compositingquality/
---
## GraphicsQualityOptions.CompositingQuality property

Obtient ou définit la qualité de rendu des images composées dessinées sur ce graphique.

```csharp
public CompositingQuality? CompositingQuality { get; set; }
```

## Exemples

Montre comment définir les options de qualité de rendu lors de la conversion de documents en formats d'image.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### Voir également

* class [GraphicsQualityOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
