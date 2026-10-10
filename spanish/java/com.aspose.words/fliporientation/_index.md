---
title: "FlipOrientation"
linktitle: "FlipOrientation"
second_title: "Aspose.Words para Java"
description: "Valores posibles para la orientación de una forma en Java."
type: docs
weight: 317
url: /es/java/com.aspose.words/fliporientation/
---

**Inheritance:**
java.lang.Object
```
public class FlipOrientation
```

Valores posibles para la orientación de una forma.

 **Examples:** 

Muestra cómo voltear una forma en un eje.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTH](#BOTH) | Voltear a lo largo de los ejes y y x. |
| [HORIZONTAL](#HORIZONTAL) | Voltear a lo largo del eje y, invirtiendo las coordenadas x. |
| [NONE](#NONE) | Las coordenadas no se voltean. |
| [VERTICAL](#VERTICAL) | Voltear a lo largo del eje x, invirtiendo las coordenadas y. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
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


Voltear a lo largo de los ejes y y x.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Voltear a lo largo del eje y, invirtiendo las coordenadas x.

### NONE {#NONE}
```
public static int NONE
```


Las coordenadas no se voltean.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Voltear a lo largo del eje x, invirtiendo las coordenadas y.

### length {#length}
```
public static int length
```


### fromName(String flipOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String flipOrientationName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flipOrientationName | java.lang.String |  |

**Returns:**
int
### fromNames(Set flipOrientationNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set flipOrientationNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flipOrientationNames | java.util.Set |  |

**Returns:**
int
### getName(int flipOrientation) {#getName-int}
```
public static String getName(int flipOrientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### getNames(int flipOrientation) {#getNames-int}
```
public static Set getNames(int flipOrientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
