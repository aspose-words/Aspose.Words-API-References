---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words pour .NET
description: Optimisez vos graphiques avec la propriété ImageSaveOptions GraphicsQualityOptions, permettant des modes de rendu précis et une qualité supérieure pour des visuels époustouflants.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Permet de spécifier le mode de rendu et la qualité pour leGraphics objet.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Remarques

Utilisez cette propriété pour remplacer les paramètres graphiques fournis par défaut par le moteur Aspose.Words.

Cela ne prendra effet que lorsqu'un document sera enregistré dans un format de type image.

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
