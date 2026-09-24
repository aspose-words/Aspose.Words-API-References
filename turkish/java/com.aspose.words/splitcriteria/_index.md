---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words Java için"
description: "Java'da belgenin parçalara nasıl bölüneceğini belirtir."
type: docs
weight: 629
url: /tr/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Belgenin bölümlere nasıl ayrılacağını belirtir.

 **Examples:** 

Belgeyi sayfalara göre nasıl bölüneceğini gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [PAGE](#PAGE) | Belgenin sayfalara bölüneceğini belirtir. |
| [SECTION_BREAK](#SECTION-BREAK) | Belgenin herhangi bir tür bölüm sonu noktasında parçalara bölüneceğini belirtir. |
| [STYLE](#STYLE) | Belgenin, [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String) içinde belirtilen stil ile biçimlendirilmiş bir paragrafta parçalara bölüneceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Belgenin sayfalara bölüneceğini belirtir.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Belgenin herhangi bir tür bölüm sonu noktasında parçalara bölüneceğini belirtir.

### STYLE {#STYLE}
```
public static int STYLE
```


Belgenin, [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String) içinde belirtilen stil ile biçimlendirilmiş bir paragrafta parçalara bölüneceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int splitCriteria) {#toString-int}
```
public static String toString(int splitCriteria)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
