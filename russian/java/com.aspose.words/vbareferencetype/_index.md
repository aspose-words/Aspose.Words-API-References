---
title: VbaReferenceType
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать тип объекта.
type: docs
weight: 599
url: /ru/java/com.aspose.words/vbareferencetype/
---

**Наследование:**
java.lang.Object
```
public class VbaReferenceType
```

 Позволяет указать тип[VbaReference](../../com.aspose.words/vbareference) объект.
## Поля

| Поле | Описание |
| --- | --- |
| [CONTROL](#CONTROL) | Определяет ссылочный тип библиотеки изменяемых типов. |
| [ORIGINAL](#ORIGINAL) | Указывает исходный ссылочный тип библиотеки типов автоматизации. |
| [PROJECT](#PROJECT) | Указан внешний тип ссылки на проект VBA. |
| [REGISTERED](#REGISTERED) | Задает ссылочный тип библиотеки типов автоматизации. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String vbaReferenceTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int vbaReferenceType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int vbaReferenceType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CONTROL {#CONTROL}
```
public static int CONTROL
```


 Определяет ссылочный тип библиотеки изменяемых типов. Этот тип соответствует 2.3.4.2.2.3 REFERENCECONTROL.[MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_файл\_formats/мс-овба/d64485fa-8562-4726-9c5e-11e8f01a81c0

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


 Указывает исходный ссылочный тип библиотеки типов автоматизации. Этот тип соответствует 2.3.4.2.2.4 REFERENCEORIGINAL Record of[MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_файл\_formats/ms-ovba/3ba66994-8c7a-4634-b2da-f9331ace6686

### PROJECT {#PROJECT}
```
public static int PROJECT
```


Указан внешний тип ссылки на проект VBA. Этот тип соответствует 2.3.4.2.2.6 REFERENCEPROJECT Record of[MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_файл\_formats/ms-ovba/08280eb0-d628-495c-867f-5985ed020142

### REGISTERED {#REGISTERED}
```
public static int REGISTERED
```


 Задает ссылочный тип библиотеки типов автоматизации. Этот тип соответствует 2.3.4.2.2.5 REFERENCEREGISTERED.[MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_файл\_formats/ms-ovba/6c39388e-96f5-4b93-b90a-ae625a063fcf

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
### fromName(String vbaReferenceTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String vbaReferenceTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaReferenceTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int vbaReferenceType) {#getName-int-}
```
public static String getName(int vbaReferenceType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaReferenceType | int |  |

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
### toString(int vbaReferenceType) {#toString-int-}
```
public static String toString(int vbaReferenceType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| vbaReferenceType | int |  |

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
