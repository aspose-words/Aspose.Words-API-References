---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет указать дополнительные java.awt.RenderingHints в Java."
type: docs
weight: 367
url: /ru/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Позволяет указать дополнительные **java.awt.RenderingHints**.

Чтобы узнать больше, посетите статью документации [ Save a Document ][Save a Document].

Получает текущие **java.awt.RenderingHints** для просмотра или добавления новых подсказок. Перезаписывает текущие **java.awt.RenderingHints**.

 **Examples:** 

Показывает, как установить параметры качества рендеринга при конвертации документов в форматы изображений.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Получает флаг, указывающий, является ли WrapMode значением TileFlipXY. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Устанавливает флаг, указывающий, является ли WrapMode значением TileFlipXY. |
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


Получает флаг, указывающий, является ли WrapMode значением TileFlipXY.

 **Remarks:** 

WrapMode определяет, как текстура или градиент заполняются плиткой, когда они меньше области заполнения.

По умолчанию используется WrapMode\#TILE.TILE (указывающий на заполнение без отражения). Это приводит к неточному рендерингу масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode на WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (указывающий, что плитки отражаются по горизонтали при перемещении вдоль строки и по вертикали при перемещении вдоль столбца).

 **Examples:** 

Показывает, как предотвратить появление белой линии при рендеринге с высоким разрешением.

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
boolean - Флаг, указывающий, является ли WrapMode значением TileFlipXY.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


Устанавливает флаг, указывающий, является ли WrapMode значением TileFlipXY.

 **Remarks:** 

WrapMode определяет, как текстура или градиент заполняются плиткой, когда они меньше области заполнения.

По умолчанию используется WrapMode\#TILE.TILE (указывающий на заполнение без отражения). Это приводит к неточному рендерингу масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode на WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (указывающий, что плитки отражаются по горизонтали при перемещении вдоль строки и по вертикали при перемещении вдоль столбца).

 **Examples:** 

Показывает, как предотвратить появление белой линии при рендеринге с высоким разрешением.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, является ли WrapMode значением TileFlipXY. |

