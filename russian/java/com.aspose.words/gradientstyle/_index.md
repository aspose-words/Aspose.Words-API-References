---
title: "GradientStyle"
linktitle: "GradientStyle"
second_title: "Aspose.Words для Java"
description: "Указывает стиль градиентной заливки в Java."
type: docs
weight: 364
url: /ru/java/com.aspose.words/gradientstyle/
---

**Inheritance:**
java.lang.Object
```
public class GradientStyle
```

Указывает стиль градиентной заливки.

 **Examples:** 

Показывает, как заполнить форму градиентом.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply One-color gradient fill to the shape with ForeColor of gradient fill.
 shape.getFill().oneColorGradient(Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2, 0.1);

 Assert.assertEquals(Color.RED.getRGB(), shape.getFill().getForeColor().getRGB());
 Assert.assertEquals(GradientStyle.HORIZONTAL, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_2, shape.getFill().getGradientVariant());
 Assert.assertEquals(270, shape.getFill().getGradientAngle());

 shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 // Apply Two-color gradient fill to the shape.
 shape.getFill().twoColorGradient(GradientStyle.FROM_CORNER, GradientVariant.VARIANT_4);
 // Change BackColor of gradient fill.
 shape.getFill().setBackColor(Color.YELLOW);
 // Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
 // gradient fill don't get any effect, it will work only for linear gradient.
 shape.getFill().setGradientAngle(15.0);

 Assert.assertEquals(Color.YELLOW.getRGB(), shape.getFill().getBackColor().getRGB());
 Assert.assertEquals(GradientStyle.FROM_CORNER, shape.getFill().getGradientStyle());
 Assert.assertEquals(GradientVariant.VARIANT_4, shape.getFill().getGradientVariant());
 Assert.assertEquals(0, shape.getFill().getGradientAngle());

 // Use the compliance option to define the shape using DML if you want to get "GradientStyle",
 // "GradientVariant" and "GradientAngle" properties after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientFill.docx", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Диагональный градиент, перемещающийся от верхнего угла к противоположному углу. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Диагональный градиент, перемещающийся от нижнего угла к противоположному углу. |
| [FROM_CENTER](#FROM-CENTER) | Градиент, идущий от центра к углам. |
| [FROM_CORNER](#FROM-CORNER) | Градиент, идущий от одного угла к трем другим углам. |
| [HORIZONTAL](#HORIZONTAL) | Градиент, идущий горизонтально через объект. |
| [NONE](#NONE) | Без градиента. |
| [VERTICAL](#VERTICAL) | Градиент, идущий вертикально вниз по объекту. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientStyle)](#toString-int) |  |
### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Диагональный градиент, перемещающийся от верхнего угла к противоположному углу.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Диагональный градиент, перемещающийся от нижнего угла к противоположному углу.

### FROM_CENTER {#FROM-CENTER}
```
public static int FROM_CENTER
```


Градиент, идущий от центра к углам.

### FROM_CORNER {#FROM-CORNER}
```
public static int FROM_CORNER
```


Градиент, идущий от одного угла к трем другим углам.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Градиент, идущий горизонтально через объект.

### NONE {#NONE}
```
public static int NONE
```


Без градиента.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Градиент, идущий вертикально вниз по объекту.

### length {#length}
```
public static int length
```


### fromName(String gradientStyleName) {#fromName-java.lang.String}
```
public static int fromName(String gradientStyleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| gradientStyleName | java.lang.String |  |

**Returns:**
int
### getName(int gradientStyle) {#getName-int}
```
public static String getName(int gradientStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int gradientStyle) {#toString-int}
```
public static String toString(int gradientStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
