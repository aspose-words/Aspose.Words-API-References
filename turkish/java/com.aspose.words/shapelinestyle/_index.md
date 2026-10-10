---
title: "ShapeLineStyle"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words Java için"
description: "Java'da bir Shape'in birleşik çizgi stilini belirtir."
type: docs
weight: 614
url: /tr/java/com.aspose.words/shapelinestyle/
---

**Inheritance:**
java.lang.Object
```
public class ShapeLineStyle
```

Bir [Shape](../../com.aspose.words/shape/) nesnesinin birleşik çizgi stilini belirtir.

 **Examples:** 

Vuruş (stroke) özelliklerinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 200.0, 200.0, WrapType.NONE);

 // Basic shapes, such as the rectangle, have two visible parts.
 // 1 -  The fill, which applies to the area within the outline of the shape:
 shape.getFill().setForeColor(Color.WHITE);

 // 2 -  The stroke, which marks the outline of the shape:
 // Modify various properties of this shape's stroke.
 Stroke stroke = shape.getStroke();
 stroke.setOn(true);
 stroke.setWeight(5.0);
 stroke.setColor(Color.RED);
 stroke.setDashStyle(DashStyle.SHORT_DASH_DOT_DOT);
 stroke.setJoinStyle(JoinStyle.MITER);
 stroke.setEndCap(EndCap.SQUARE);
 stroke.setLineStyle(ShapeLineStyle.TRIPLE);
 stroke.getFill().twoColorGradient(Color.RED, Color.BLUE, GradientStyle.VERTICAL, GradientVariant.VARIANT_1);

 doc.save(getArtifactsDir() + "Shape.Stroke.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DEFAULT](#DEFAULT) | Varsayılan değer [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE) dir. |
| [DOUBLE](#DOUBLE) | Eşit genişlikte çift çizgiler. |
| [SINGLE](#SINGLE) | Tek çizgi. |
| [THICK_THIN](#THICK-THIN) | Birisi kalın, birisi ince olan çift çizgiler. |
| [THIN_THICK](#THIN-THICK) | Birisi ince, birisi kalın olan çift çizgiler. |
| [TRIPLE](#TRIPLE) | Üç çizgi, ince, kalın, ince. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String shapeLineStyleName)](#fromName-java.lang.String) |  |
| [getName(int shapeLineStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeLineStyle)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [SINGLE](../../com.aspose.words/shapelinestyle/\#SINGLE) dir.

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Eşit genişlikte çift çizgiler.

### SINGLE {#SINGLE}
```
public static int SINGLE
```


Tek çizgi.

### THICK_THIN {#THICK-THIN}
```
public static int THICK_THIN
```


Birisi kalın, birisi ince olan çift çizgiler.

### THIN_THICK {#THIN-THICK}
```
public static int THIN_THICK
```


Birisi ince, birisi kalın olan çift çizgiler.

### TRIPLE {#TRIPLE}
```
public static int TRIPLE
```


Üç çizgi, ince, kalın, ince.

### length {#length}
```
public static int length
```


### fromName(String shapeLineStyleName) {#fromName-java.lang.String}
```
public static int fromName(String shapeLineStyleName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeLineStyleName | java.lang.String |  |

**Returns:**
int
### getName(int shapeLineStyle) {#getName-int}
```
public static String getName(int shapeLineStyle)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeLineStyle) {#toString-int}
```
public static String toString(int shapeLineStyle)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeLineStyle | int |  |

**Returns:**
java.lang.String
