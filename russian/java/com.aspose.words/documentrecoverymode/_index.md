---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words для Java"
description: "Указывает доступные варианты восстановления, когда документ сталкивается с ошибками при загрузке в Java."
type: docs
weight: 171
url: /ru/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

Указывает доступные варианты восстановления, когда документ сталкивается с ошибками во время загрузки.

 **Examples:** 

Показывает, как попытаться восстановить документ, если во время загрузки произошли ошибки.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Восстановление не производится. |
| [TRY_RECOVER](#TRY-RECOVER) | Пытается восстановить документ, сохраняя как можно больше данных. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Восстановление не производится. Если документ недействителен, загрузка завершится ошибкой.

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


Пытается восстановить документ, сохраняя как можно больше данных.

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
