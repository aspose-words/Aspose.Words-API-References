---
title: MailMergeDataType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип внешнего источника данных слияния почты.
type: docs
weight: 382
url: /ru/java/com.aspose.words/mailmergedatatype/
---

**Наследование:**
java.lang.Object
```
public class MailMergeDataType
```

Указывает тип внешнего источника данных слияния почты.
## Поля

| Поле | Описание |
| --- | --- |
| [DATABASE](#DATABASE) | Указывает, что данный документ был подключен к базе данных Access через систему динамического обмена данными (DDE). |
| [DEFAULT](#DEFAULT) |  Равно[NONE](../../com.aspose.words/mailmergedatatype\#NONE). |
| [NATIVE](#NATIVE) | Указывает, что данный документ был подключен к внешнему источнику данных через интерфейс объекта источника данных Office (ODSO). |
| [NONE](#NONE) | Источник данных слияния не указан. |
| [ODBC](#ODBC) | Указывает, что данный документ был подключен к внешнему источнику данных через интерфейс Open Database Connectivity. |
| [QUERY](#QUERY) | Указывает, что данный документ был подключен к внешнему источнику данных с помощью внешнего инструмента запросов. |
| [SPREADSHEET](#SPREADSHEET) | Указывает, что данный документ был подключен к электронной таблице Excel через систему динамического обмена данными (DDE). |
| [TEXT_FILE](#TEXT-FILE) | Указывает, что данный документ был подключен к текстовому файлу через систему динамического обмена данными (DDE). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int mailMergeDataType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int mailMergeDataType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Указывает, что данный документ был подключен к базе данных Access через систему динамического обмена данными (DDE).

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Равно[NONE](../../com.aspose.words/mailmergedatatype\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Указывает, что данный документ был подключен к внешнему источнику данных через интерфейс объекта источника данных Office (ODSO).

### NONE {#NONE}
```
public static int NONE
```


Источник данных слияния не указан.

### ODBC {#ODBC}
```
public static int ODBC
```


Указывает, что данный документ был подключен к внешнему источнику данных через интерфейс Open Database Connectivity.

### QUERY {#QUERY}
```
public static int QUERY
```


Указывает, что данный документ был подключен к внешнему источнику данных с помощью внешнего инструмента запросов.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Указывает, что данный документ был подключен к электронной таблице Excel через систему динамического обмена данными (DDE).

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Указывает, что данный документ был подключен к текстовому файлу через систему динамического обмена данными (DDE).

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeDataTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int mailMergeDataType) {#getName-int-}
```
public static String getName(int mailMergeDataType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int mailMergeDataType) {#toString-int-}
```
public static String toString(int mailMergeDataType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
