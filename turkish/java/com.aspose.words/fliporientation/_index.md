---
title: "FlipOrientation"
linktitle: "FlipOrientation"
second_title: "Aspose.Words Java için"
description: "Java'da bir şeklin yönelimi için olası değerler."
type: docs
weight: 317
url: /tr/java/com.aspose.words/fliporientation/
---

**Inheritance:**
java.lang.Object
```
public class FlipOrientation
```

Bir şeklin yönelimi için olası değerler.

 **Examples:** 

Bir şekli bir eksende nasıl çevireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert an image shape and leave its orientation in its default state.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 Assert.assertEquals(FlipOrientation.NONE, shape.getFlipOrientation());

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 250.0,
         RelativeVerticalPosition.TOP_MARGIN, 100.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
 // making it into a horizontal mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.HORIZONTAL);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 100.0,
         RelativeVerticalPosition.TOP_MARGIN, 250.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
 // making it into a vertical mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.VERTICAL);

 shape = builder.insertShape(ShapeType.RECTANGLE, RelativeHorizontalPosition.LEFT_MARGIN, 250.0,
         RelativeVerticalPosition.TOP_MARGIN, 250.0, 100.0, 100.0, WrapType.NONE);
 shape.getImageData().setImage(getImageDir() + "Logo.jpg");

 // Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
 // making it into a horizontal and vertical mirror image of the first shape.
 shape.setFlipOrientation(FlipOrientation.BOTH);

 doc.save(getArtifactsDir() + "Shape.FlipShapeOrientation.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTH](#BOTH) | y ve x eksenleri boyunca çevir. |
| [HORIZONTAL](#HORIZONTAL) | y ekseni boyunca çevir, x koordinatlarını tersine çevir. |
| [NONE](#NONE) | Koordinatlar çevrilmez. |
| [VERTICAL](#VERTICAL) | x ekseni boyunca çevir, y koordinatlarını tersine çevir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String flipOrientationName)](#fromName-java.lang.String) |  |
| [fromNames(Set flipOrientationNames)](#fromNames-java.util.Set) |  |
| [getName(int flipOrientation)](#getName-int) |  |
| [getNames(int flipOrientation)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int flipOrientation)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


y ve x eksenleri boyunca çevir.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


y ekseni boyunca çevir, x koordinatlarını tersine çevir.

### NONE {#NONE}
```
public static int NONE
```


Koordinatlar çevrilmez.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


x ekseni boyunca çevir, y koordinatlarını tersine çevir.

### length {#length}
```
public static int length
```


### fromName(String flipOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String flipOrientationName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| flipOrientationName | java.lang.String |  |

**Returns:**
int
### fromNames(Set flipOrientationNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set flipOrientationNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| flipOrientationNames | java.util.Set |  |

**Returns:**
int
### getName(int flipOrientation) {#getName-int}
```
public static String getName(int flipOrientation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### getNames(int flipOrientation) {#getNames-int}
```
public static Set getNames(int flipOrientation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int flipOrientation) {#toString-int}
```
public static String toString(int flipOrientation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
