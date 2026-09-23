---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Angeben zusätzlicher java.awt.RenderingHints in Java."
type: docs
weight: 367
url: /de/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Ermöglicht das Angeben zusätzlicher **java.awt.RenderingHints**.

Um mehr zu erfahren, besuchen Sie den [ Save a Document ][Save a Document] Dokumentationsartikel.

Ermittelt die aktuellen **java.awt.RenderingHints**, um sie anzuzeigen oder neue Hinweise hinzuzufügen. Überschreibt die aktuellen **java.awt.RenderingHints**.

 **Examples:** 

Zeigt, wie man Renderqualitätsoptionen beim Konvertieren von Dokumenten in Bildformate festlegt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Gibt ein Flag zurück, das angibt, ob WrapMode TileFlipXY ist. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Setzt ein Flag, das angibt, ob WrapMode TileFlipXY ist. |
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


Gibt ein Flag zurück, das angibt, ob WrapMode TileFlipXY ist.

 **Remarks:** 

Der WrapMode gibt an, wie eine Textur oder ein Farbverlauf gekachelt wird, wenn sie kleiner ist als der zu füllende Bereich.

Verwendet standardmäßig WrapMode\#TILE.TILE (gibt Kachelung ohne Spiegelung an). Dies führt zu ungenauer Darstellung des skalierten Bildes (mit hoher Auflösung).

Diese Eigenschaft ermöglicht das Umschalten von WrapMode zu WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (gibt an, dass Kacheln horizontal umgekehrt werden, wenn man entlang einer Zeile bewegt, und vertikal, wenn man entlang einer Spalte bewegt).

 **Examples:** 

Zeigt, wie man verhindert, dass beim Rendern mit hoher Auflösung eine weiße Linie erscheint.

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
boolean – Ein Flag, das angibt, ob WrapMode TileFlipXY ist.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


Setzt ein Flag, das angibt, ob WrapMode TileFlipXY ist.

 **Remarks:** 

Der WrapMode gibt an, wie eine Textur oder ein Farbverlauf gekachelt wird, wenn sie kleiner ist als der zu füllende Bereich.

Verwendet standardmäßig WrapMode\#TILE.TILE (gibt Kachelung ohne Spiegelung an). Dies führt zu ungenauer Darstellung des skalierten Bildes (mit hoher Auflösung).

Diese Eigenschaft ermöglicht das Umschalten von WrapMode zu WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (gibt an, dass Kacheln horizontal umgekehrt werden, wenn man entlang einer Zeile bewegt, und vertikal, wenn man entlang einer Spalte bewegt).

 **Examples:** 

Zeigt, wie man verhindert, dass beim Rendern mit hoher Auflösung eine weiße Linie erscheint.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob WrapMode TileFlipXY ist. |

