---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.GraphicsQualityOptions pour améliorer la qualité graphique des documents avec des options personnalisables pour une sortie supérieure.
type: docs
weight: 5790
url: /fr/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

Permet de spécifier des informations supplémentairesGraphics options de qualité.

Pour en savoir plus, visitez le[Enregistrer un document](https://docs.aspose.com/words/net/save-a-document/) article de documentation.

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
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | Obtient ou définit une valeur qui spécifie comment les images composées sont dessinées sur ce graphique. |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | Obtient ou définit la qualité de rendu des images composées dessinées sur ce graphique. |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | Obtient ou définit le mode d'interpolation associé à ce graphique. |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | Obtient ou définit la qualité de rendu de ce graphique. |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | Obtient ou définit les informations de mise en page du texte (telles que l'alignement, l'orientation et les taquets de tabulation), les manipulations d'affichage (telles que l'insertion de points de suspension et la substitution de chiffres nationaux) et les fonctionnalités OpenType. |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | Obtient ou définit le mode de rendu du texte associé à ce graphique. |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | Obtient ou définit un indicateur indiquant si WrapMode est TileFlipXY. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
