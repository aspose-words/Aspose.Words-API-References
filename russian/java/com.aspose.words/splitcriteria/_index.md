---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words для Java"
description: "Указывает, как документ разбивается на части в Java."
type: docs
weight: 629
url: /ru/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Указывает, как документ разбивается на части.

 **Examples:** 

Показывает, как разбить документ по страницам.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [PAGE](#PAGE) | Указывает, что документ разбивается на страницы. |
| [SECTION_BREAK](#SECTION-BREAK) | Указывает, что документ разбивается на части при разрыве раздела любого типа. |
| [STYLE](#STYLE) | Указывает, что документ разбивается на части в абзаце, отформатированном с использованием стиля, указанного в [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Указывает, что документ разбивается на страницы.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Указывает, что документ разбивается на части при разрыве раздела любого типа.

### STYLE {#STYLE}
```
public static int STYLE
```


Указывает, что документ разбивается на части в абзаце, отформатированном с использованием стиля, указанного в [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
