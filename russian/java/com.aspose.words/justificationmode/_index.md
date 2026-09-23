---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words для Java"
description: "Указывает настройку межсимвольного интервала для документа в Java."
type: docs
weight: 411
url: /ru/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Указывает настройку межсимвольного интервала для документа. Значение по умолчанию —  Expand .

 **Examples:** 

Показывает, как управлять контролем межсимвольного интервала.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [COMPRESS](#COMPRESS) | Сжать межсимвольный интервал. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Сжать, используя правила кана‑словарей, хираганы и катаканы. |
| [EXPAND](#EXPAND) | Не сжимать межсимвольный интервал. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Сжать межсимвольный интервал.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Сжать, используя правила кана‑словарей, хираганы и катаканы.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


Не сжимать межсимвольный интервал.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
