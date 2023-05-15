---
title: GradientStyle
linktitle: GradientStyle
second_title: Aspose.Words for Java
description: Specifies the style for a gradient fill in Java.
type: docs
weight: 322
url: /java/com.aspose.words/gradientstyle/
---

**Inheritance:**
java.lang.Object
```
public class GradientStyle
```

Specifies the style for a gradient fill.

 **Examples:** 

Shows how to fill a shape with a gradients.

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
## Fields

| Field | Description |
| --- | --- |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Diagonal gradient moving from a top corner down to the opposite corner. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Diagonal gradient moving from a bottom corner up to the opposite corner. |
| [FROM_CENTER](#FROM-CENTER) | Gradient running from the center out to the corners. |
| [FROM_CORNER](#FROM-CORNER) | Gradient running from a corner to the other three corners. |
| [HORIZONTAL](#HORIZONTAL) | Gradient running horizontally across an object. |
| [NONE](#NONE) | No gradient. |
| [VERTICAL](#VERTICAL) | Gradient running vertically down an object. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int gradientStyle)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Diagonal gradient moving from a top corner down to the opposite corner.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Diagonal gradient moving from a bottom corner up to the opposite corner.

### FROM_CENTER {#FROM-CENTER}
```
public static int FROM_CENTER
```


Gradient running from the center out to the corners.

### FROM_CORNER {#FROM-CORNER}
```
public static int FROM_CORNER
```


Gradient running from a corner to the other three corners.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Gradient running horizontally across an object.

### NONE {#NONE}
```
public static int NONE
```


No gradient.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Gradient running vertically down an object.

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
### fromName(String gradientStyleName) {#fromName-java.lang.String}
```
public static int fromName(String gradientStyleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientStyleName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int gradientStyle) {#getName-int}
```
public static String getName(int gradientStyle)
```




**Parameters:**
| Parameter | Type | Description |
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
### toString(int gradientStyle) {#toString-int}
```
public static String toString(int gradientStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientStyle | int |  |

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

