---
title: "GradientVariant"
linktitle: "GradientVariant"
second_title: "Aspose.Words Java için"
description: "Java'da bir degrade doldurma için varyantı belirtir."
type: docs
weight: 365
url: /tr/java/com.aspose.words/gradientvariant/
---

**Inheritance:**
java.lang.Object
```
public class GradientVariant
```

Bir degrade doldurma için varyantı belirtir.

 **Remarks:** 

Word'deki Doldurma Efektleri iletişim kutusundaki Degrade sekmesindeki dört varyanta karşılık gelir.

 **Examples:** 

Bir şekli gradientlerle doldurmanın nasıl yapılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Degrade varyantı 'None'. |
| [VARIANT_1](#VARIANT-1) | Degrade varyantı 1. |
| [VARIANT_2](#VARIANT-2) | Degrade varyantı 2. |
| [VARIANT_3](#VARIANT-3) | Degrade varyantı 3. |
| [VARIANT_4](#VARIANT-4) | Degrade varyantı 4. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String gradientVariantName)](#fromName-java.lang.String) |  |
| [getName(int gradientVariant)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int gradientVariant)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Degrade varyantı 'None'.

### VARIANT_1 {#VARIANT-1}
```
public static int VARIANT_1
```


Degrade varyantı 1.

### VARIANT_2 {#VARIANT-2}
```
public static int VARIANT_2
```


Degrade varyantı 2.

### VARIANT_3 {#VARIANT-3}
```
public static int VARIANT_3
```


Degrade varyantı 3.

 **Remarks:** 

Bu varyant, [GradientStyle.FROM\\_CENTER](../../com.aspose.words/gradientstyle/\\#FROM-CENTER) stilindeki degrade doldurmaya, nesne işaretleme dili [ShapeMarkupLanguage.VML](../../com.aspose.words/shapemarkuplanguage/\\#VML) ise, uygulanamaz.

### VARIANT_4 {#VARIANT-4}
```
public static int VARIANT_4
```


Degrade varyantı 4.

 **Remarks:** 

Bu varyant, [GradientStyle.FROM\\_CENTER](../../com.aspose.words/gradientstyle/\\#FROM-CENTER) stilindeki degrade doldurmaya, nesne işaretleme dili [ShapeMarkupLanguage.VML](../../com.aspose.words/shapemarkuplanguage/\\#VML) ise, uygulanamaz.

### length {#length}
```
public static int length
```


### fromName(String gradientVariantName) {#fromName-java.lang.String}
```
public static int fromName(String gradientVariantName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| gradientVariantName | java.lang.String |  |

**Returns:**
int
### getName(int gradientVariant) {#getName-int}
```
public static String getName(int gradientVariant)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| gradientVariant | int |  |

**Returns:**
java.lang.String
