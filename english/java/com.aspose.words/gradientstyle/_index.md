---
title: GradientStyle
linktitle: GradientStyle
second_title: Aspose.Words for Java
description: Specifies the style for a gradient fill in Java.
type: docs
weight: 356
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
| [fromName(String gradientStyleName)](#fromName-java.lang.String) |  |
| [getName(int gradientStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientStyle)](#toString-int) |  |
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
