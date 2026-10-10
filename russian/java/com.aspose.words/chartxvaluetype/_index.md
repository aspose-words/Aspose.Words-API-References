---
title: "ChartXValueType"
linktitle: "ChartXValueType"
second_title: "Aspose.Words для Java"
description: "Позволяет указать тип X‑значения серии диаграммы в Java."
type: docs
weight: 96
url: /ru/java/com.aspose.words/chartxvaluetype/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValueType
```

Позволяет указать тип значения X серии диаграммы.
## Поля

| Поле | Описание |
| --- | --- |
| [DATE_TIME](#DATE-TIME) | Указывает, что X‑значение представляет дату и время суток. |
| [DOUBLE](#DOUBLE) | Указывает, что X‑значение является числом двойной точности с плавающей запятой. |
| [MULTILEVEL](#MULTILEVEL) | Указывает, что X‑значение является многоуровневым значением. |
| [STRING](#STRING) | Указывает, что X‑значение является строковой категорией. |
| [TIME](#TIME) | Указывает, что X‑значение представляет время суток. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chartXValueTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartXValueType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartXValueType)](#toString-int) |  |
### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


Указывает, что X‑значение представляет дату и время суток.

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Указывает, что X‑значение является числом двойной точности с плавающей запятой.

### MULTILEVEL {#MULTILEVEL}
```
public static int MULTILEVEL
```


Указывает, что X‑значение является многоуровневым значением.

### STRING {#STRING}
```
public static int STRING
```


Указывает, что X‑значение является строковой категорией.

### TIME {#TIME}
```
public static int TIME
```


Указывает, что X‑значение представляет время суток.

### length {#length}
```
public static int length
```


### fromName(String chartXValueTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartXValueTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartXValueTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartXValueType) {#getName-int}
```
public static String getName(int chartXValueType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartXValueType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartXValueType) {#toString-int}
```
public static String toString(int chartXValueType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartXValueType | int |  |

**Returns:**
java.lang.String
