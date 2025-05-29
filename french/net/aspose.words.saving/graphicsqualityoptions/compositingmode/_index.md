---
title: GraphicsQualityOptions.CompositingMode
linktitle: CompositingMode
articleTitle: CompositingMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété GraphicsQualityOptions CompositingMode pour optimiser le rendu des images, améliorant ainsi les performances et la qualité de vos graphiques.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Obtient ou définit une valeur qui spécifie comment les images composées sont dessinées sur ce graphique.

```csharp
public CompositingMode? CompositingMode { get; set; }
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
