---
title: GradientVariant
second_title: Aspose.Words for Java API Reference
description: Specifies the variant for a gradient fill.
type: docs
weight: 311
url: /java/com.aspose.words/gradientvariant/
---

**Inheritance:**
java.lang.Object
```
public class GradientVariant
```

Specifies the variant for a gradient fill. Corresponds to the four variants on the Gradient tab in the Fill Effects dialog box in Word.
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
| [getName(int gradientVariant)](#getName-int-) |  |
| [toString(int gradientVariant)](#toString-int-) |  |
| [fromName(String gradientVariantName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
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


Gradient variant 3. This variant is not applicable to gradient fill with the style [GradientStyle.FROM\_CENTER](../../com.aspose.words/gradientstyle\#FROM-CENTER), if object has markup language [ShapeMarkupLanguage.VML](../../com.aspose.words/shapemarkuplanguage\#VML).

### VARIANT_4 {#VARIANT-4}
```
public static int VARIANT_4
```


Gradient variant 4. This variant is not applicable to gradient fill with the style [GradientStyle.FROM\_CENTER](../../com.aspose.words/gradientstyle\#FROM-CENTER), if object has markup language [ShapeMarkupLanguage.VML](../../com.aspose.words/shapemarkuplanguage\#VML).

### length {#length}
```
public static int length
```


### getName(int gradientVariant) {#getName-int-}
```
public static String getName(int gradientVariant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientVariant | int |  |

**Returns:**
java.lang.String
### toString(int gradientVariant) {#toString-int-}
```
public static String toString(int gradientVariant)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientVariant | int |  |

**Returns:**
java.lang.String
### fromName(String gradientVariantName) {#fromName-java.lang.String-}
```
public static int fromName(String gradientVariantName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientVariantName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
