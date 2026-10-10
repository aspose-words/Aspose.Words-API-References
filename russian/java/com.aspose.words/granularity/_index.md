---
title: "Granularity"
linktitle: "Granularity"
second_title: "Aspose.Words для Java"
description: "Указывает гранулярность изменений, которые следует отслеживать при сравнении двух документов в Java."
type: docs
weight: 366
url: /ru/java/com.aspose.words/granularity/
---

**Inheritance:**
java.lang.Object
```
public class Granularity
```

Указывает степень детализации изменений для отслеживания при сравнении двух документов.

 **Examples:** 

Показывает, как указать гранулярность при сравнении документов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CHAR_LEVEL](#CHAR-LEVEL) | Указывает изменения на уровне символов. |
| [WORD_LEVEL](#WORD-LEVEL) | Указывает изменения на уровне слова. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String granularityName)](#fromName-java.lang.String) |  |
| [getName(int granularity)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int granularity)](#toString-int) |  |
### CHAR_LEVEL {#CHAR-LEVEL}
```
public static int CHAR_LEVEL
```


Указывает изменения на уровне символов.

### WORD_LEVEL {#WORD-LEVEL}
```
public static int WORD_LEVEL
```


Указывает изменения на уровне слова.

### length {#length}
```
public static int length
```


### fromName(String granularityName) {#fromName-java.lang.String}
```
public static int fromName(String granularityName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| granularityName | java.lang.String |  |

**Returns:**
int
### getName(int granularity) {#getName-int}
```
public static String getName(int granularity)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| granularity | int |  |

**Returns:**
java.lang.String
