---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier des java.awt.RenderingHints supplémentaires en Java."
type: docs
weight: 367
url: /fr/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Permet de spécifier des **java.awt.RenderingHints** supplémentaires.

Pour en savoir plus, consultez l'article de documentation [ Save a Document ][Save a Document].

Obtient les **java.awt.RenderingHints** actuels pour les visualiser ou ajouter de nouveaux indices. Remplace les **java.awt.RenderingHints** actuels.

 **Examples:** 

Montre comment définir les options de qualité de rendu lors de la conversion de documents en formats d'image.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions();
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON); // SmoothingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON); // TextRenderingHint
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_COLOR_RENDERING, RenderingHints.VALUE_COLOR_RENDER_QUALITY); // CompositingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_RENDERING, RenderingHints.VALUE_RENDER_QUALITY); // CompositingQuality
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_INTERPOLATION, RenderingHints.VALUE_INTERPOLATION_BILINEAR); // InterpolationMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_FRACTIONALMETRICS, RenderingHints.VALUE_FRACTIONALMETRICS_ON); // StringFormat

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 saveOptions.setGraphicsQualityOptions(qualityOptions);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Obtient un indicateur indiquant si WrapMode est TileFlipXY. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Définit un indicateur indiquant si WrapMode est TileFlipXY. |
### getRenderingHints() {#getRenderingHints}
```
public RenderingHints getRenderingHints()
```




**Returns:**
java.awt.RenderingHints
### getUseTileFlipMode() {#getUseTileFlipMode}
```
public boolean getUseTileFlipMode()
```


Obtient un indicateur indiquant si WrapMode est TileFlipXY.

 **Remarks:** 

Le WrapMode spécifie comment une texture ou un dégradé est répété lorsqu'il est plus petit que la zone à remplir.

Par défaut, utilise WrapMode\\#TILE.TILE (spécifie un carrelage sans retournement). Cela entraîne un rendu inexact de l'image mise à l'échelle (avec haute résolution).

Cette propriété permet de changer le WrapMode en WrapMode\\#TILE\\_FLIP\\_XY.TILE\\_FLIP\\_XY (spécifie que les carreaux sont retournés horizontalement lorsque vous vous déplacez le long d'une ligne et retournés verticalement lorsque vous vous déplacez le long d'une colonne).

 **Examples:** 

Montre comment empêcher l'apparition d'une ligne blanche lors du rendu avec une haute résolution.

```

 Document doc = new Document(getMyDir() + "Shape high dpi.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShapeRenderer renderer = shape.getShapeRenderer();

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
 {
     saveOptions.setResolution(500f); saveOptions.setGraphicsQualityOptions(new GraphicsQualityOptions()); { saveOptions.getGraphicsQualityOptions().setUseTileFlipMode(true); }
 }
 renderer.save(getArtifactsDir() + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
 
```

**Returns:**
boolean - Un indicateur indiquant si WrapMode est TileFlipXY.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


Définit un indicateur indiquant si WrapMode est TileFlipXY.

 **Remarks:** 

Le WrapMode spécifie comment une texture ou un dégradé est répété lorsqu'il est plus petit que la zone à remplir.

Par défaut, utilise WrapMode\\#TILE.TILE (spécifie un carrelage sans retournement). Cela entraîne un rendu inexact de l'image mise à l'échelle (avec haute résolution).

Cette propriété permet de changer le WrapMode en WrapMode\\#TILE\\_FLIP\\_XY.TILE\\_FLIP\\_XY (spécifie que les carreaux sont retournés horizontalement lorsque vous vous déplacez le long d'une ligne et retournés verticalement lorsque vous vous déplacez le long d'une colonne).

 **Examples:** 

Montre comment empêcher l'apparition d'une ligne blanche lors du rendu avec une haute résolution.

```

 Document doc = new Document(getMyDir() + "Shape high dpi.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShapeRenderer renderer = shape.getShapeRenderer();

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
 {
     saveOptions.setResolution(500f); saveOptions.setGraphicsQualityOptions(new GraphicsQualityOptions()); { saveOptions.getGraphicsQualityOptions().setUseTileFlipMode(true); }
 }
 renderer.save(getArtifactsDir() + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Un indicateur indiquant si WrapMode est TileFlipXY. |

