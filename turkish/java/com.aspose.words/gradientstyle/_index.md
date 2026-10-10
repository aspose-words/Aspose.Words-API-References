---
title: "GradientStyle"
linktitle: "GradientStyle"
second_title: "Aspose.Words Java için"
description: "Java'da bir degrade doldurma stili belirtir."
type: docs
weight: 364
url: /tr/java/com.aspose.words/gradientstyle/
---

**Inheritance:**
java.lang.Object
```
public class GradientStyle
```

Bir degrade doldurma için stili belirtir.

 **Examples:** 

Bir şekli gradientlerle doldurmanın nasıl yapılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Üst köşeden karşı köşeye doğru hareket eden diyagonal gradient. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Alt köşeden karşı köşeye doğru hareket eden diyagonal gradient. |
| [FROM_CENTER](#FROM-CENTER) | Gradientin merkezden köşelere doğru yayılması. |
| [FROM_CORNER](#FROM-CORNER) | Gradientin bir köşeden diğer üç köşeye doğru yayılması. |
| [HORIZONTAL](#HORIZONTAL) | Gradientin bir nesne boyunca yatay olarak akması. |
| [NONE](#NONE) | Gradient yok. |
| [VERTICAL](#VERTICAL) | Gradientin bir nesne boyunca dikey olarak aşağı akması. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientStyle)](#toString-int) |  |
### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Üst köşeden karşı köşeye doğru hareket eden diyagonal gradient.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Alt köşeden karşı köşeye doğru hareket eden diyagonal gradient.

### FROM_CENTER {#FROM-CENTER}
```
public static int FROM_CENTER
```


Gradientin merkezden köşelere doğru yayılması.

### FROM_CORNER {#FROM-CORNER}
```
public static int FROM_CORNER
```


Gradientin bir köşeden diğer üç köşeye doğru yayılması.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Gradientin bir nesne boyunca yatay olarak akması.

### NONE {#NONE}
```
public static int NONE
```


Gradient yok.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Gradientin bir nesne boyunca dikey olarak aşağı akması.

### length {#length}
```
public static int length
```


### fromName(String gradientStyleName) {#fromName-java.lang.String}
```
public static int fromName(String gradientStyleName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| gradientStyleName | java.lang.String |  |

**Returns:**
int
### getName(int gradientStyle) {#getName-int}
```
public static String getName(int gradientStyle)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| gradientStyle | int |  |

**Returns:**
java.lang.String
