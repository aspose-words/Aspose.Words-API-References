---
title: FlipOrientation
linktitle: FlipOrientation
second_title: Aspose.Words for Java
description: Possible values for the orientation of a shape in Java.
type: docs
weight: 285
url: /java/com.aspose.words/fliporientation/
---

**Inheritance:**
java.lang.Object
```
public class FlipOrientation
```

Possible values for the orientation of a shape.

 **Examples:** 

Shows how to flip a shape on an axis.

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
## Fields

| Field | Description |
| --- | --- |
| [BOTH](#BOTH) | Flip along both the y- and x-axis. |
| [HORIZONTAL](#HORIZONTAL) | Flip along the y-axis, reversing the x-coordinates. |
| [NONE](#NONE) | Coordinates are not flipped. |
| [VERTICAL](#VERTICAL) | Flip along the x-axis, reversing the y-coordinates. |
| [length](#length) |  |
## Methods

| Method | Description |
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


Flip along both the y- and x-axis.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Flip along the y-axis, reversing the x-coordinates.

### NONE {#NONE}
```
public static int NONE
```


Coordinates are not flipped.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Flip along the x-axis, reversing the y-coordinates.

### length {#length}
```
public static int length
```


### fromName(String flipOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String flipOrientationName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| flipOrientationName | java.lang.String |  |

**Returns:**
int
### fromNames(Set flipOrientationNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set flipOrientationNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| flipOrientationNames | java.util.Set |  |

**Returns:**
int
### getName(int flipOrientation) {#getName-int}
```
public static String getName(int flipOrientation)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### getNames(int flipOrientation) {#getNames-int}
```
public static Set getNames(int flipOrientation)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
