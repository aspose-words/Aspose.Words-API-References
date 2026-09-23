---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words для Java"
description: "Описывает уровни формирования, требуемые скриптом в Java."
type: docs
weight: 598
url: /ru/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Описывает уровни формирования, требуемые скриптом.
## Поля

| Поле | Описание |
| --- | --- |
| [FULL](#FULL) | Скрипт требует полной поддержки формирования. |
| [MINIMUM](#MINIMUM) | Скрипт требует минимальной поддержки формирования. |
| [NONE](#NONE) | Скрипт не требует формирования. |
| [UNKNOWN](#UNKNOWN) | Это используется, когда уровень для скрипта не указан. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


Скрипт требует полной поддержки формирования.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Скрипт требует минимальной поддержки формирования.

 **Remarks:** 

Неясно, что означает Minimum. Minimum устанавливается для некоторых очень популярных скриптов (Latin, Cyrillic...).

### NONE {#NONE}
```
public static int NONE
```


Скрипт не требует формирования.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Это используется, когда уровень для скрипта не указан.

 **Remarks:** 

Этого не должно происходить.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int scriptShapingLevel) {#toString-int}
```
public static String toString(int scriptShapingLevel)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
