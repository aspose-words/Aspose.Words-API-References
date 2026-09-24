---
title: "EmphasisMark"
linktitle: "EmphasisMark"
second_title: "Aspose.Words Java için"
description: "Java'da olası vurgu işareti türlerini belirtir."
type: docs
weight: 187
url: /tr/java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Vurgu işaretinin olası türlerini belirtir.

 **Examples:** 

Glif karakterinin üstüne/altına ek bir karakter eklemenin nasıl yapılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Vurgu işareti yok. |
| [OVER_COMMA](#OVER-COMMA) | Vurgu işareti, metnin üzerinde görüntülenen bir virgül karakteridir. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | Vurgu işareti, metnin üzerinde görüntülenen dolu siyah bir dairedir. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | Vurgu işareti, metnin üzerinde görüntülenen boş beyaz bir dairedir. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | Vurgu işareti, metnin altında görüntülenen dolu siyah bir dairedir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Vurgu işareti yok.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


Vurgu işareti, metnin üzerinde görüntülenen bir virgül karakteridir.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


Vurgu işareti, metnin üzerinde görüntülenen dolu siyah bir dairedir.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


Vurgu işareti, metnin üzerinde görüntülenen boş beyaz bir dairedir.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


Vurgu işareti, metnin altında görüntülenen dolu siyah bir dairedir.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
