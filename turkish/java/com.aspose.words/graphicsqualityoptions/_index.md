---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words Java için"
description: "Java'da ek java.awt.RenderingHints belirtmeye izin verir."
type: docs
weight: 367
url: /tr/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Ek **java.awt.RenderingHints** belirtmeye izin verir.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

Mevcut **java.awt.RenderingHints**'i görüntülemek veya yeni ipuçları eklemek için alır. Mevcut **java.awt.RenderingHints**'i üzerine yazar.

 **Examples:** 

Belgeleri görüntü formatlarına dönüştürürken render kalite seçeneklerinin nasıl ayarlanacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | WrapMode'un TileFlipXY olup olmadığını gösteren bir bayrak alır. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | WrapMode'un TileFlipXY olup olmadığını gösteren bir bayrak ayarlar. |
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


WrapMode'un TileFlipXY olup olmadığını gösteren bir bayrak alır.

 **Remarks:** 

WrapMode, bir doku veya degrade doldurulan alandan daha küçük olduğunda nasıl döşeneceğini belirtir.

Varsayılan olarak WrapMode\#TILE.TILE kullanılır (döndürmeden döşemeyi belirtir). Bu, ölçeklenmiş görüntünün (yüksek çözünürlükte) hatalı render edilmesine neden olur.

Bu özellik, WrapMode'u WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY olarak değiştirmeye izin verir (karoların bir satır boyunca hareket ederken yatay olarak ve bir sütun boyunca hareket ederken dikey olarak çevrildiğini belirtir).

 **Examples:** 

Yüksek çözünürlükte render ederken ortaya çıkan beyaz çizgiyi nasıl önleyeceğinizi gösterir.

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
boolean - WrapMode'un TileFlipXY olup olmadığını gösteren bir bayrak.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


WrapMode'un TileFlipXY olup olmadığını gösteren bir bayrak ayarlar.

 **Remarks:** 

WrapMode, bir doku veya degrade doldurulan alandan daha küçük olduğunda nasıl döşeneceğini belirtir.

Varsayılan olarak WrapMode\#TILE.TILE kullanılır (döndürmeden döşemeyi belirtir). Bu, ölçeklenmiş görüntünün (yüksek çözünürlükte) hatalı render edilmesine neden olur.

Bu özellik, WrapMode'u WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY olarak değiştirmeye izin verir (karoların bir satır boyunca hareket ederken yatay olarak ve bir sütun boyunca hareket ederken dikey olarak çevrildiğini belirtir).

 **Examples:** 

Yüksek çözünürlükte render ederken ortaya çıkan beyaz çizgiyi nasıl önleyeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | WrapMode'un TileFlipXY olup olmadığını gösteren bir bayrak. |

