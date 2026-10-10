---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد java.awt.RenderingHints إضافية في Java."
type: docs
weight: 367
url: /ar/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

يسمح بتحديد **java.awt.RenderingHints** إضافية.

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

يحصل على **java.awt.RenderingHints** الحالية للعرض أو لإضافة تلميحات جديدة. يكتب فوق **java.awt.RenderingHints** الحالية.

 **Examples:** 

يوضح كيفية ضبط خيارات جودة العرض أثناء تحويل المستندات إلى صيغ الصور.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | يحصل على علم يشير إلى ما إذا كان WrapMode هو TileFlipXY. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | يضبط علمًا يشير إلى ما إذا كان WrapMode هو TileFlipXY. |
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


يحصل على علم يشير إلى ما إذا كان WrapMode هو TileFlipXY.

 **Remarks:** 

يحدد WrapMode كيفية تكرار النسيج أو التدرج عندما يكون أصغر من المنطقة التي يتم ملؤها.

بشكل افتراضي يستخدم WrapMode\#TILE.TILE (يحدد التكرار دون انعكاس). هذا يسبب عرضًا غير دقيق للصورة المُقاسة (بدقة عالية).

هذه الخاصية تسمح بتبديل WrapMode إلى WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (يحدد أن البلاطات تُقلب أفقياً عند الانتقال على طول الصف وتُقلب عمودياً عند الانتقال على طول العمود).

 **Examples:** 

يوضح كيفية منع ظهور الخط الأبيض عند العرض بدقة عالية.

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
boolean - علم يشير إلى ما إذا كان WrapMode هو TileFlipXY.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان WrapMode هو TileFlipXY.

 **Remarks:** 

يحدد WrapMode كيفية تكرار النسيج أو التدرج عندما يكون أصغر من المنطقة التي يتم ملؤها.

بشكل افتراضي يستخدم WrapMode\#TILE.TILE (يحدد التكرار دون انعكاس). هذا يسبب عرضًا غير دقيق للصورة المُقاسة (بدقة عالية).

هذه الخاصية تسمح بتبديل WrapMode إلى WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (يحدد أن البلاطات تُقلب أفقياً عند الانتقال على طول الصف وتُقلب عمودياً عند الانتقال على طول العمود).

 **Examples:** 

يوضح كيفية منع ظهور الخط الأبيض عند العرض بدقة عالية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان WrapMode هو TileFlipXY. |

