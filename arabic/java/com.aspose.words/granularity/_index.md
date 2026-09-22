---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words لـ Java"
description: "يحدد درجة تفصيل التغييرات التي يجب تتبعها عند مقارنة مستندين في Java."
type: docs
weight: 366
url: /ar/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

يحدد دقة التغييرات التي يجب تتبعها عند مقارنة مستندين.

 **Examples:** 

يظهر لتحديد درجة التفصيل أثناء مقارنة المستندات.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | يحدد التغييرات على مستوى الأحرف. |
| [WORD_LEVEL](#WORD-LEVEL) | يحدد التغييرات على مستوى الكلمة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


يحدد التغييرات على مستوى الأحرف.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


يحدد التغييرات على مستوى الكلمة.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
