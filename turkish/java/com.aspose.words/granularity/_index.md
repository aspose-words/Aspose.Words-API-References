---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words Java için"
description: "Java'da iki belgeyi karşılaştırırken izlenecek değişikliklerin granülerliğini belirtir."
type: docs
weight: 366
url: /tr/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

İki belgeyi karşılaştırırken izlenecek değişikliklerin ayrıntı seviyesini belirtir.

 **Examples:** 

Belgeleri karşılaştırırken bir granülerlik belirtmeyi gösterir.

```

 Document docA = new Document();
 DocumentBuilder builderA = new DocumentBuilder(docA);
 builderA.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

 Document docB = new Document();
 DocumentBuilder builderB = new DocumentBuilder(docB);
 builderB.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

 // Specify whether changes are tracking
 // by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setGranularity(granularity);

 docA.compare(docB, "author", new Date(), compareOptions);

 // The first document's collection of revision groups contains all the differences between documents.
 RevisionGroupCollection groups = docA.getRevisions().getGroups();
 Assert.assertEquals(5, groups.getCount());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | Değişiklikleri karakter düzeyinde belirtir. |
| [WORD_LEVEL](#WORD-LEVEL) | Kelime seviyesinde değişiklikleri belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


Değişiklikleri karakter düzeyinde belirtir.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


Kelime seviyesinde değişiklikleri belirtir.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int granularity) {#toString-int}
```
public static String toString(int granularity)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
