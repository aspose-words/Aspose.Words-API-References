---
title: "FlipOrientation"
linktitle: "FlipOrientation"
second_title: "Aspose.Words لـ Java"
description: "القيم المحتملة لتوجيه الشكل في Java."
type: docs
weight: 317
url: /ar/java/com.aspose.words/fliporientation/
---

**Inheritance:**
java.lang.Object
```
public class FlipOrientation
```

القيم المحتملة لتوجيه الشكل.

 **Examples:** 

يوضح كيفية عكس الشكل على محور.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTH](#BOTH) | عكس على كل من المحور y والمحور x. |
| [HORIZONTAL](#HORIZONTAL) | عكس على المحور y، مع عكس إحداثيات x. |
| [NONE](#NONE) | الإحداثيات غير مقلوبة. |
| [VERTICAL](#VERTICAL) | عكس على المحور x، مع عكس إحداثيات y. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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


عكس على كل من المحور y والمحور x.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


عكس على المحور y، مع عكس إحداثيات x.

### NONE {#NONE}
```
public static int NONE
```


الإحداثيات غير مقلوبة.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


عكس على المحور x، مع عكس إحداثيات y.

### length {#length}
```
public static int length
```


### fromName(String flipOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String flipOrientationName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| flipOrientationName | java.lang.String |  |

**Returns:**
int
### fromNames(Set flipOrientationNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set flipOrientationNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| flipOrientationNames | java.util.Set |  |

**Returns:**
int
### getName(int flipOrientation) {#getName-int}
```
public static String getName(int flipOrientation)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### getNames(int flipOrientation) {#getNames-int}
```
public static Set getNames(int flipOrientation)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| flipOrientation | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
