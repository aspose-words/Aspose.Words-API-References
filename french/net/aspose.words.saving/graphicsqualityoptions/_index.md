---
title: Class GraphicsQualityOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.GraphicsQualityOptions classe. Permet de spécifier desGraphics options de qualité.
type: docs
weight: 4780
url: /fr/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Permet de spécifier desGraphics options de qualité.

```csharp
public class GraphicsQualityOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Obtient ou définit une valeur qui spécifie comment les images composées sont dessinées sur ce Graphics. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Obtient ou définit la qualité de rendu des images composites dessinées sur ce Graphics. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Obtient ou définit le mode d'interpolation associé à ce Graphics. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Obtient ou définit la qualité de rendu de ce Graphics. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Obtient ou définit les informations de mise en page du texte (telles que l'alignement, l'orientation et les taquets de tabulation), les manipulations d'affichage (telles que l'insertion de points de suspension et la substitution de chiffres nationaux) et les fonctionnalités OpenType. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Obtient ou définit le mode de rendu du texte associé à ce Graphics. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Obtient ou définit un indicateur indiquant si WrapMode est TileFlipXY. |

### Exemples

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


