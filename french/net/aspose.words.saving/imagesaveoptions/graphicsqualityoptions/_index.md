---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words pour .NET
description: ImageSaveOptions GraphicsQualityOptions propriété. Permet de spécifier le mode et la qualité du rendu pour leGraphics objet en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

Permet de spécifier le mode et la qualité du rendu pour leGraphics objet.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## Remarques

Utilisez cette propriété pour remplacer les paramètres graphiques fournis par défaut par le moteur Aspose.Words.

Cela ne prendra effet que lorsqu'un document est enregistré dans un format semblable à une image.

## Exemples

Montre comment définir les options de qualité de rendu lors de la conversion de documents aux formats d'image.

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
