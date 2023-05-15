---
title: WrapSide
linktitle: WrapSide
second_title: Aspose.Words for Java
description: Specifies what sides of the shape or picture the text wraps around in Java.
type: docs
weight: 641
url: /java/com.aspose.words/wrapside/
---

**Inheritance:**
java.lang.Object
```
public class WrapSide
```

Specifies what side(s) of the shape or picture the text wraps around.

 **Examples:** 

Shows how to replace all textbox shapes with image shapes.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOTH](#BOTH) | The document text wraps on both sides of the shape. |
| [DEFAULT](#DEFAULT) | Default value is [BOTH](../../com.aspose.words/wrapside/\#BOTH). |
| [LARGEST](#LARGEST) | The document text wraps on the side of the shape that is farthest from the page margin, leaving text free area on the other side of the shape. |
| [LEFT](#LEFT) | The document text wraps on the left side of the shape only. |
| [RIGHT](#RIGHT) | The document text wraps on the right side of the shape only. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String wrapSideName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int wrapSide)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int wrapSide)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


The document text wraps on both sides of the shape.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value is [BOTH](../../com.aspose.words/wrapside/\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


The document text wraps on the side of the shape that is farthest from the page margin, leaving text free area on the other side of the shape.

### LEFT {#LEFT}
```
public static int LEFT
```


The document text wraps on the left side of the shape only. There is a text free area on the right of the shape.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


The document text wraps on the right side of the shape only. There is a text free area on the left side of the shape.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String wrapSideName) {#fromName-java.lang.String}
```
public static int fromName(String wrapSideName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int wrapSide) {#getName-int}
```
public static String getName(int wrapSide)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int wrapSide) {#toString-int}
```
public static String toString(int wrapSide)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapSide | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

