---
title: MailMergeDestination
second_title: Справочник по API Aspose.Words для Java
description: Определяет возможные результаты, которые могут быть получены при выполнении слияния для документа.
type: docs
weight: 383
url: /ru/java/com.aspose.words/mailmergedestination/
---

**Наследование:**
java.lang.Object
```
public class MailMergeDestination
```

Определяет возможные результаты, которые могут быть получены при выполнении слияния для документа.
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) |  Равно[NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination\#NEW-DOCUMENT) ценность. |
| [EMAIL](#EMAIL) | Указывает, что соответствующие приложения хостинга должны генерировать электронные письма с использованием документов, полученных в результате заполнения полей в данном документе данными из указанного внешнего источника данных. |
| [FAX](#FAX) | Указывает, что соответствующие приложения хостинга должны генерировать факсы с использованием документов, полученных в результате заполнения полей в заданном документе данными из указанного внешнего источника данных. |
| [NEW_DOCUMENT](#NEW-DOCUMENT) | Указывает, что соответствующие приложения размещения должны генерировать новые документы, заполняя поля в заданном документе данными из указанного внешнего источника данных. |
| [PRINTER](#PRINTER) | Указывает, что соответствующие хост-приложения должны печатать документы, полученные в результате заполнения полей в заданном документе внешними данными из указанного внешнего источника данных. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String mailMergeDestinationName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int mailMergeDestination)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int mailMergeDestination)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Равно[NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination\#NEW-DOCUMENT) ценность.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Указывает, что соответствующие приложения хостинга должны генерировать электронные письма с использованием документов, полученных в результате заполнения полей в данном документе данными из указанного внешнего источника данных.

### FAX {#FAX}
```
public static int FAX
```


Указывает, что соответствующие приложения хостинга должны генерировать факсы с использованием документов, полученных в результате заполнения полей в заданном документе данными из указанного внешнего источника данных.

### NEW_DOCUMENT {#NEW-DOCUMENT}
```
public static int NEW_DOCUMENT
```


Указывает, что соответствующие приложения размещения должны генерировать новые документы, заполняя поля в заданном документе данными из указанного внешнего источника данных.

### PRINTER {#PRINTER}
```
public static int PRINTER
```


Указывает, что соответствующие хост-приложения должны печатать документы, полученные в результате заполнения полей в заданном документе внешними данными из указанного внешнего источника данных.

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
### fromName(String mailMergeDestinationName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeDestinationName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDestinationName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int mailMergeDestination) {#getName-int-}
```
public static String getName(int mailMergeDestination)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDestination | int |  |

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
### toString(int mailMergeDestination) {#toString-int-}
```
public static String toString(int mailMergeDestination)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDestination | int |  |

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
