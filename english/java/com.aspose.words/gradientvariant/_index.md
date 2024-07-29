---
title: GradientVariant
linktitle: GradientVariant
second_title: Aspose.Words for Java
description: Specifies the variant for a gradient fill in Java.
type: docs
weight: 341
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
| [fromName(String gradientVariantName)](#fromName-java.lang.String) |  |
| [getName(int gradientVariant)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientVariant)](#toString-int) |  |
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
