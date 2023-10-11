---
title: GraphicsQualityOptions.UseTileFlipMode
second_title: Référence de l'API Aspose.Words pour .NET
description: GraphicsQualityOptions propriété. Obtient ou définit un indicateur indiquant si WrapMode est TileFlipXY.
type: docs
weight: 80
url: /fr/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Obtient ou définit un indicateur indiquant si WrapMode est TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

### Remarques

LeWrapMode spécifie comment une texture ou un dégradé est carrelé lorsqu'il est plus petit que la zone à remplir.

Par défaut utiliseTile (spécifie le carrelage sans retournement). Cela provoque un rendu inexact de l'image mise à l'échelle (avec une haute résolution).

Cette propriété permet de passer WrapMode àTileFlipXY (spécifie que les tuiles sont retournées horizontalement lorsque vous vous déplacez le long d'une ligne et retournées verticalement lorsque vous vous déplacez le long d'une colonne).

### Exemples

Montre comment éviter l'apparition d'une ligne blanche lors d'un rendu avec une haute résolution.

```csharp
Document doc = new Document(MyDir + "Shape high dpi.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShapeRenderer renderer = shape.GetShapeRenderer();

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
{
    Resolution = 500, GraphicsQualityOptions = new GraphicsQualityOptions { UseTileFlipMode = true }
};
renderer.Save(ArtifactsDir + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
```

### Voir également

* class [GraphicsQualityOptions](../)
* espace de noms [Aspose.Words.Saving](../../graphicsqualityoptions/)
* Assemblée [Aspose.Words](../../../)


