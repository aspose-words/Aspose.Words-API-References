---
title: "VariationAxis"
linktitle: "VariationAxis"
second_title: "Aspose.Words Java için"
description: "Java'da OpenType Tasarım-Varyasyon Eksen Etiketini temsil eder."
type: docs
weight: 704
url: /tr/java/com.aspose.words/variationaxis/
---

**Inheritance:**
java.lang.Object
```
public class VariationAxis
```

OpenType Tasarım-Varyasyon Eksen Etiketini temsil eder. https://learn.microsoft.com/en-us/typography/opentype/spec/dvaraxisreg
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ITALIC](#ITALIC) | Roman/eğik eksen için kayıtlı etiket. |
| [OPTICAL_SIZE](#OPTICAL-SIZE) | Optik-boyut ekseni için kayıtlı etiket. |
| [SLANT](#SLANT) | Eğim ekseni için kayıtlı etiket. |
| [WEIGHT](#WEIGHT) | Ağırlık ekseni için kayıtlı etiket. |
| [WIDTH](#WIDTH) | Genişlik ekseni için kayıtlı etiket. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String variationAxisName)](#fromName-java.lang.String) |  |
| [getName(int variationAxis)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int variationAxis)](#toString-int) |  |
### ITALIC {#ITALIC}
```
public static int ITALIC
```


Roman/eğik eksen için kayıtlı etiket.

### OPTICAL_SIZE {#OPTICAL-SIZE}
```
public static int OPTICAL_SIZE
```


Optik-boyut ekseni için kayıtlı etiket. Not: Optik-boyut ekseni, OpenType boyut özelliğinin yerini alır.

### SLANT {#SLANT}
```
public static int SLANT
```


Eğim ekseni için kayıtlı etiket.

### WEIGHT {#WEIGHT}
```
public static int WEIGHT
```


Ağırlık ekseni için kayıtlı etiket.

### WIDTH {#WIDTH}
```
public static int WIDTH
```


Genişlik ekseni için kayıtlı etiket.

### length {#length}
```
public static int length
```


### fromName(String variationAxisName) {#fromName-java.lang.String}
```
public static int fromName(String variationAxisName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| variationAxisName | java.lang.String |  |

**Returns:**
int
### getName(int variationAxis) {#getName-int}
```
public static String getName(int variationAxis)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| variationAxis | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int variationAxis) {#toString-int}
```
public static String toString(int variationAxis)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| variationAxis | int |  |

**Returns:**
java.lang.String
