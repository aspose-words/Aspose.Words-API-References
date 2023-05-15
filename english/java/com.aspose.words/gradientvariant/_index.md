---
title: GradientVariant
linktitle: GradientVariant
second_title: Aspose.Words for Java
description: Specifies the variant for a gradient fill in Java.
type: docs
weight: 323
url: /java/com.aspose.words/gradientvariant/
---

**Inheritance:**
java.lang.Object
```
public class GradientVariant
```

Specifies the variant for a gradient fill.

 **Remarks:** 

Corresponds to the four variants on the Gradient tab in the Fill Effects dialog box in Word.

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
| [NONE](#NONE) | Gradient variant 'None'. |
| [VARIANT_1](#VARIANT-1) | Gradient variant 1. |
| [VARIANT_2](#VARIANT-2) | Gradient variant 2. |
| [VARIANT_3](#VARIANT-3) | Gradient variant 3. |
| [VARIANT_4](#VARIANT-4) | Gradient variant 4. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String gradientVariantName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int gradientVariant)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int gradientVariant)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Gradient variant 'None'.

### VARIANT_1 {#VARIANT-1}
```
public static int VARIANT_1
```


Gradient variant 1.

### VARIANT_2 {#VARIANT-2}
```
public static int VARIANT_2
```


Gradient variant 2.

### VARIANT_3 {#VARIANT-3}
```
public static int VARIANT_3
```


Gradient variant 3.

 **Remarks:** 

This variant is not applicable to gradient fill with the style [GradientStyle.FROM\_CENTER](../../com.aspose.words/gradientstyle/\#FROM-CENTER), if object has markup language [ShapeMarkupLanguage.VML](../../com.aspose.words/shapemarkuplanguage/\#VML).

### VARIANT_4 {#VARIANT-4}
```
public static int VARIANT_4
```


Gradient variant 4.

 **Remarks:** 

This variant is not applicable to gradient fill with the style [GradientStyle.FROM\_CENTER](../../com.aspose.words/gradientstyle/\#FROM-CENTER), if object has markup language [ShapeMarkupLanguage.VML](../../com.aspose.words/shapemarkuplanguage/\#VML).

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
### fromName(String gradientVariantName) {#fromName-java.lang.String}
```
public static int fromName(String gradientVariantName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientVariantName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int gradientVariant) {#getName-int}
```
public static String getName(int gradientVariant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientVariant | int |  |

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
### toString(int gradientVariant) {#toString-int}
```
public static String toString(int gradientVariant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientVariant | int |  |

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

