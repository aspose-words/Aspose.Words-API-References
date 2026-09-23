---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words для Java"
description: "Указывает тип внешнего источника данных, к которому следует подключиться в рамках информации о соединении ODSO в Java."
type: docs
weight: 488
url: /ru/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

Указывает тип внешнего источника данных, к которому следует подключиться в рамках информации о соединении ODSO.

 **Remarks:** 

Спецификация OOXML очень расплывчата для этого перечисления. Полагаю, она может соответствовать перечислению WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Поля

| Поле | Описание |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Указывает, что данный документ был подключён к адресной книге контактов. |
| [DATABASE](#DATABASE) | Указывает, что данный документ был подключён к базе данных. |
| [DEFAULT](#DEFAULT) | Равно [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Указывает, что данный документ был подключён к другому формату документа, поддерживаемому приложением‑создателем. |
| [DOCUMENT_2](#DOCUMENT-2) | Указывает, что данный документ был подключён к другому формату документа, поддерживаемому приложением‑создателем. |
| [EMAIL](#EMAIL) | Указывает, что данный документ был подключён к почтовому приложению. |
| [LEGACY](#LEGACY) | Указывает, что данный документ был подключён к устаревшему формату документа, поддерживаемому приложением‑создателем. Возможно wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Указывает, что данный документ был подключён к источнику данных, который агрегирует другие источники данных. |
| [NATIVE](#NATIVE) | Указывает, что данный документ был подключён к другому формату документа, родному приложению‑создателю. |
| [NONE](#NONE) | Тип внешнего источника данных не указан. |
| [TEXT](#TEXT) | Указывает, что данный документ был подключён к текстовому файлу. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Указывает, что данный документ был подключён к адресной книге контактов. Возможно wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Указывает, что данный документ был подключён к базе данных. Возможно wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Равно [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Указывает, что данный документ был подключён к другому формату документа, поддерживаемому приложением‑создателем. Возможно wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Указывает, что данный документ был подключён к другому формату документа, поддерживаемому приложением‑создателем. Возможно wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Указывает, что данный документ был подключён к почтовому приложению. Возможно wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Указывает, что данный документ был подключён к устаревшему формату документа, поддерживаемому приложением‑создателем. Возможно wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Указывает, что данный документ был подключён к источнику данных, который агрегирует другие источники данных.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Указывает, что данный документ был подключён к другому формату документа, родному приложению‑создателю. Возможно wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


Тип внешнего источника данных не указан. Возможно wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Указывает, что данный документ был подключён к текстовому файлу. Возможно wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
