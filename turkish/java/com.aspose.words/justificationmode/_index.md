---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge için karakter aralığı ayarlamasını belirtir."
type: docs
weight: 411
url: /tr/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Bir belge için karakter aralığı ayarlamasını belirtir. Varsayılan değer Expand.

 **Examples:** 

Karakter aralığı kontrolünü nasıl yöneteceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [COMPRESS](#COMPRESS) | Karakter aralığını sıkıştır. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Kana hece sistemlerinin kurallarını kullanarak, Hiragana ve Katakana'yı sıkıştır. |
| [EXPAND](#EXPAND) | Karakter aralığını sıkıştırma. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Karakter aralığını sıkıştır.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Kana hece sistemlerinin kurallarını kullanarak, Hiragana ve Katakana'yı sıkıştır.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


Karakter aralığını sıkıştırma.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int justificationMode) {#toString-int}
```
public static String toString(int justificationMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
