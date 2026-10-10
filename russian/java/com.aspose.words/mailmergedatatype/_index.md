---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words для Java"
description: "Указывает тип внешнего источника данных слияния почты в Java."
type: docs
weight: 440
url: /ru/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Указывает тип внешнего источника данных слияния почты.
## Поля

| Поле | Описание |
| --- | --- |
| [DATABASE](#DATABASE) | Указывает, что данный документ был подключён к базе данных Access через систему Dynamic Data Exchange (DDE). |
| [DEFAULT](#DEFAULT) | Равен [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Указывает, что данный документ был подключён к внешнему источнику данных через интерфейс Office Data Source Object (ODSO). |
| [NONE](#NONE) | Источник данных слияния почты не указан. |
| [ODBC](#ODBC) | Указывает, что данный документ был подключён к внешнему источнику данных через интерфейс Open Database Connectivity. |
| [QUERY](#QUERY) | Указывает, что данный документ был подключён к внешнему источнику данных с помощью внешнего инструмента запросов. |
| [SPREADSHEET](#SPREADSHEET) | Указывает, что данный документ был подключён к таблице Excel через систему Dynamic Data Exchange (DDE). |
| [TEXT_FILE](#TEXT-FILE) | Указывает, что данный документ был подключён к текстовому файлу через систему Dynamic Data Exchange (DDE). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Указывает, что данный документ был подключён к базе данных Access через систему Dynamic Data Exchange (DDE).

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Равен [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Указывает, что данный документ был подключён к внешнему источнику данных через интерфейс Office Data Source Object (ODSO).

### NONE {#NONE}
```
public static int NONE
```


Источник данных слияния почты не указан.

### ODBC {#ODBC}
```
public static int ODBC
```


Указывает, что данный документ был подключён к внешнему источнику данных через интерфейс Open Database Connectivity.

### QUERY {#QUERY}
```
public static int QUERY
```


Указывает, что данный документ был подключён к внешнему источнику данных с помощью внешнего инструмента запросов.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Указывает, что данный документ был подключён к таблице Excel через систему Dynamic Data Exchange (DDE).

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Указывает, что данный документ был подключён к текстовому файлу через систему Dynamic Data Exchange (DDE).

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDataType) {#toString-int}
```
public static String toString(int mailMergeDataType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
