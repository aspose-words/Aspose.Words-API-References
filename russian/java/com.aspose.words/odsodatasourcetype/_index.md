---
title: OdsoDataSourceType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть информации о соединении ODSO.
type: docs
weight: 412
url: /ru/java/com.aspose.words/odsodatasourcetype/
---

**Наследование:**
java.lang.Object
```
public class OdsoDataSourceType
```

Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть информации о соединении ODSO.

Спецификация OOXML для этого перечисления очень расплывчата. Я предполагаю, что это может соответствовать перечислению WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Поля

| Поле | Описание |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Указывает, что данный документ был подключен к адресной книге контактов. |
| [DATABASE](#DATABASE) | Указывает, что данный документ был подключен к базе данных. |
| [DEFAULT](#DEFAULT) |  Равно[NONE](../../com.aspose.words/odsodatasourcetype\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | Указывает, что данный документ был связан с другим форматом документа, поддерживаемым создающим приложением. |
| [DOCUMENT_2](#DOCUMENT-2) | Указывает, что данный документ был связан с другим форматом документа, поддерживаемым создающим приложением. |
| [EMAIL](#EMAIL) | Указывает, что данный документ был подключен к приложению электронной почты. |
| [LEGACY](#LEGACY) | Указывает, что данный документ был подключен к устаревшему формату документа, поддерживаемому создающим приложением. Возможно, wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Указывает, что данный документ был подключен к источнику данных, который объединяет другие источники данных. |
| [NATIVE](#NATIVE) | Указывает, что данный документ был связан с другим форматом документа, родным для создающего приложения. |
| [NONE](#NONE) | Тип внешнего источника данных не указан. |
| [TEXT](#TEXT) | Указывает, что данный документ был подключен к текстовому файлу. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int odsoDataSourceType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int odsoDataSourceType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Указывает, что данный документ был подключен к адресной книге контактов. Возможно, wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Указывает, что данный документ был подключен к базе данных. Возможно, wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Равно[NONE](../../com.aspose.words/odsodatasourcetype\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Указывает, что данный документ был связан с другим форматом документа, поддерживаемым создающим приложением. Возможно, wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Указывает, что данный документ был связан с другим форматом документа, поддерживаемым создающим приложением. Возможно, wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Указывает, что данный документ был подключен к приложению электронной почты. Возможно, wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Указывает, что данный документ был подключен к устаревшему формату документа, поддерживаемому создающим приложением. Возможно, wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Указывает, что данный документ был подключен к источнику данных, который объединяет другие источники данных.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Указывает, что данный документ был связан с другим форматом документа, родным для создающего приложения. Возможно, wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


Тип внешнего источника данных не указан. Возможно, вдмержесубтипеворд.

### TEXT {#TEXT}
```
public static int TEXT
```


Указывает, что данный документ был подключен к текстовому файлу. Возможно, wdMergeSubTypeOther.

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
### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int odsoDataSourceType) {#getName-int-}
```
public static String getName(int odsoDataSourceType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| odsoDataSourceType | int |  |

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
### toString(int odsoDataSourceType) {#toString-int-}
```
public static String toString(int odsoDataSourceType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| odsoDataSourceType | int |  |

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
