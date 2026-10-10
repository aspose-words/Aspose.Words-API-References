---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare ulteriori java.awt.RenderingHints in Java."
type: docs
weight: 367
url: /it/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Consente di specificare ulteriori **java.awt.RenderingHints**.

Per saperne di più, visita l'articolo di documentazione [ Save a Document ][Save a Document].

Ottiene gli **java.awt.RenderingHints** correnti per visualizzarli o aggiungere nuovi suggerimenti. Sovrascrive gli **java.awt.RenderingHints** correnti.

 **Examples:** 

Mostra come impostare le opzioni di qualità di rendering durante la conversione dei documenti in formati immagine.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Ottiene un flag che indica se WrapMode è TileFlipXY. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Imposta un flag che indica se WrapMode è TileFlipXY. |
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


Ottiene un flag che indica se WrapMode è TileFlipXY.

 **Remarks:** 

Il WrapMode specifica come una trama o un gradiente viene ripetuto quando è più piccolo dell'area da riempire.

Per impostazione predefinita utilizza WrapMode\#TILE.TILE (specifica il tiling senza capovolgimento). Questo causa un rendering impreciso dell'immagine scalata (con alta risoluzione).

Questa proprietà consente di passare WrapMode a WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifica che le tessere vengono capovolte orizzontalmente man mano che ci si sposta lungo una riga e verticalmente man mano che ci si sposta lungo una colonna).

 **Examples:** 

Mostra come impedire che appaia la linea bianca durante il rendering ad alta risoluzione.

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
boolean - Un flag che indica se WrapMode è TileFlipXY.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


Imposta un flag che indica se WrapMode è TileFlipXY.

 **Remarks:** 

Il WrapMode specifica come una trama o un gradiente viene ripetuto quando è più piccolo dell'area da riempire.

Per impostazione predefinita utilizza WrapMode\#TILE.TILE (specifica il tiling senza capovolgimento). Questo causa un rendering impreciso dell'immagine scalata (con alta risoluzione).

Questa proprietà consente di passare WrapMode a WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifica che le tessere vengono capovolte orizzontalmente man mano che ci si sposta lungo una riga e verticalmente man mano che ci si sposta lungo una colonna).

 **Examples:** 

Mostra come impedire che appaia la linea bianca durante il rendering ad alta risoluzione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un flag che indica se WrapMode è TileFlipXY. |

