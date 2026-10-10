---
title: "ShapeRenderer"
linktitle: "ShapeRenderer"
second_title: "Aspose.Words для Java"
description: "Предоставляет методы для рендеринга отдельного Shape или GroupShape в растровое или векторное изображение или в объект Graphics в Java."
type: docs
weight: 616
url: /ru/java/com.aspose.words/shaperenderer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeRendererBase](../../com.aspose.words/noderendererbase/)
```
public class ShapeRenderer extends NodeRendererBase
```

Предоставляет методы для рендеринга отдельного [Shape](../../com.aspose.words/shape/) или [GroupShape](../../com.aspose.words/groupshape/) в растровое или векторное изображение или в объект Graphics.

Чтобы узнать больше, посетите статью документации [ Working with Shapes ][Working with Shapes].


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ShapeRenderer(ShapeBase shape)](#ShapeRenderer-com.aspose.words.ShapeBase) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float) | Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getBoundsInPoints()](#getBoundsInPoints) | Возвращает фактические границы фигуры в пунктах. |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float) | Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints) | Возвращает непрозрачные границы фигуры в пунктах. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getSizeInPoints()](#getSizeInPoints) | Возвращает фактический размер фигуры в пунктах. |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float) | Отрисовывает фигуру в объект java.awt.Graphics2D с указанным масштабом. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float) | Отрисовывает фигуру в объект java.awt.Graphics2D с указанным размером. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions) |  |
| [save(OutputStream stream, SvgSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions) | Отрисовывает фигуру и сохраняет её в изображение. |
| [save(String fileName, SvgSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SvgSaveOptions) | Отрисовывает фигуру и сохраняет её в SVG‑изображение. |
### ShapeRenderer(ShapeBase shape) {#ShapeRenderer-com.aspose.words.ShapeBase}
```
public ShapeRenderer(ShapeBase shape)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| shape | [ShapeBase](../../com.aspose.words/shapebase/) | Объект DrawinML shape, который вы хотите отрисовать. |

### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 **Remarks:** 

Этот метод преобразует [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) в прямоугольник в пикселях.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| dpi | float | Разрешение (горизонтальное и вертикальное) для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Rectangle — Фактический (как отрисовано на странице) ограничивающий прямоугольник фигуры в пикселях.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 **Remarks:** 

Этот метод преобразует [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) в прямоугольник в пикселях.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Rectangle — Фактический (как отрисовано на странице) ограничивающий прямоугольник фигуры в пикселях.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


Возвращает фактические границы фигуры в пунктах.

 **Remarks:** 

Это свойство возвращает фактический (как отрисовано на странице) ограничивающий прямоугольник фигуры. Границы учитывают вращение фигуры (если есть).

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float — Фактические границы фигуры в пунктах.
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 **Remarks:** 

Этот метод преобразует [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) в прямоугольник в пикселях и полезен, когда вы хотите создать битмап для рендеринга фигуры только с её непрозрачной частью.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| dpi | float | Разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Rectangle - Непрозрачный прямоугольник фигуры в пикселях.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет непрозрачные границы фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 **Remarks:** 

Этот метод преобразует [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) в прямоугольник в пикселях и полезен, когда вы хотите создать битмап для рендеринга фигуры только с её непрозрачной частью.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Rectangle - Непрозрачный прямоугольник фигуры в пикселях.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


Возвращает непрозрачные границы фигуры в пунктах.

 **Remarks:** 

Это свойство возвращает непрозрачный (т.е. прозрачные части фигуры игнорируются) ограничивающий прямоугольник фигуры. При вычислении границ учитывается вращение фигуры.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - Непрозрачные границы фигуры в пунктах.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 **Remarks:** 

Этот метод преобразует [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) в размер в пикселях и полезен, когда вы хотите создать битмап для аккуратного рендеринга фигуры на битмапе.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| dpi | float | Разрешение (горизонтальное и вертикальное) для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Dimension - Размер фигуры в пикселях.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет размер фигуры в пикселях для указанного коэффициента масштабирования и разрешения.

 **Remarks:** 

Этот метод преобразует [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) в размер в пикселях и полезен, когда вы хотите создать битмап для аккуратного рендеринга фигуры на битмапе.

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| масштаб | float | Коэффициент масштабирования (1.0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования из пунктов в пиксели (точек на дюйм). |

**Returns:**
java.awt.Dimension - Размер фигуры в пикселях.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Возвращает фактический размер фигуры в пунктах.

 **Remarks:** 

Это свойство возвращает размер фактического (как отрисовано на странице) ограничивающего прямоугольника фигуры. При вычислении размера учитывается вращение фигуры (если есть).

 **Examples:** 

Показывает, как измерять и масштабировать фигуры.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Point2D.Float - Фактический размер фигуры в пунктах.
### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


Отрисовывает фигуру в объект java.awt.Graphics2D с указанным масштабом.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| графика | java.awt.Graphics2D | Объект, в который производится рендеринг. |
| x | float | Координата X (в мировых единицах) верхнего левого угла отрисованной фигуры. |
| y | float | Координата Y (в мировых единицах) верхнего левого угла отрисованной фигуры. |
| масштаб | float | Масштаб для рендеринга фигуры (1.0 соответствует 100%). |

**Returns:**
java.awt.geom.Point2D.Float - Ширина и высота (в мировых единицах) отрисованной фигуры.
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


Отрисовывает фигуру в объект java.awt.Graphics2D с указанным размером.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| графика | java.awt.Graphics2D | Объект, в который производится рендеринг. |
| x | float | Координата X (в мировых единицах) верхнего левого угла отрисованной фигуры. |
| y | float | Координата Y (в мировых единицах) верхнего левого угла отрисованной фигуры. |
| ширина | float | Максимальная ширина (в мировых единицах), которую может занимать отрисованная фигура. |
| высота | float | Максимальная высота (в мировых единицах), которую может занимать отрисованная фигура. |

**Returns:**
float - Масштаб, который был автоматически рассчитан для отрисованной фигуры, чтобы она соответствовала указанному размеру.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |

### save(OutputStream stream, SvgSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions}
```
public void save(OutputStream stream, SvgSaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


Отрисовывает фигуру и сохраняет её в изображение.  Отрисовывает фигуру в изображение и сохраняет в файл.

 **Examples:** 

Показывает, как отрисовать объект Office Math в файл изображения в локальной файловой системе.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
 // how it renders the OfficeMath node into an image.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Scale" property to 5 to render the object to five times its original size.
 saveOptions.setScale(5f);

 math.getMathRenderer().save(getArtifactsDir() + "Shape.RenderOfficeMath.png", saveOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл будет перезаписан. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Указывает параметры, которые контролируют, как фигура рендерится и сохраняется. Может быть `null`. |

### save(String fileName, SvgSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SvgSaveOptions}
```
public void save(String fileName, SvgSaveOptions saveOptions)
```


Рендерит фигуру и сохраняет её в SVG‑изображение. Рендерит фигуру в SVG‑изображение и сохраняет в файл.

 **Examples:** 

Показывает, как передать параметры сохранения при рендеринге офисных формул.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath)doc.getChild(NodeType.OFFICE_MATH, 0, true);

 SvgSaveOptions options = new SvgSaveOptions();
 options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);

 math.getMathRenderer().save(getArtifactsDir() + "SvgSaveOptions.Output.svg", options);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл будет перезаписан. |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) | Указывает параметры, которые контролируют, как фигура рендерится и сохраняется. Может быть `null`. |

