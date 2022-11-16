---
title: VbaReference
second_title: Справочник по API Aspose.Words для Java
description: Реализует ссылку на библиотеку типов автоматизации или проект VBA.
type: docs
weight: 597
url: /ru/java/com.aspose.words/vbareference/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

Реализует ссылку на библиотеку типов автоматизации или проект VBA.

 Чтобы узнать больше, посетите**Working with VBA Macros** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [VbaReference()](#VbaReference--) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getLibId()](#getLibId--) | Получает строковое значение, содержащее идентификатор библиотеки типов автоматизации. |
| [getType()](#getType--) |  Получает[VbaReferenceType](../../com.aspose.words/vbareferencetype) объект, указывающий тип ссылки, которую представляет объект VbaReference. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### VbaReference() {#VbaReference--}
```
public VbaReference()
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getLibId() {#getLibId--}
```
public abstract String getLibId()
```


Получает строковое значение, содержащее идентификатор библиотеки типов автоматизации. В зависимости от типа ссылки значение этого свойства может быть:

 *   LibidReference, указанный в 2.1.1.8 LibidReference of[MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_файл\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *   ProjectReference, указанный в 2.1.1.12 ProjectReference of[MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_файл\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

**Возвращает:**
java.lang.String — строковое значение, содержащее идентификатор библиотеки типов автоматизации.
### getType() {#getType--}
```
public abstract int getType()
```


 Получает[VbaReferenceType](../../com.aspose.words/vbareferencetype) объект, указывающий тип ссылки, которую представляет объект VbaReference.

**Возвращает:**
 инт -\{[VbaReferenceType](../../com.aspose.words/vbareferencetype) объект, указывающий тип ссылки, которую представляет объект VbaReference. Возвращаемое значение является одним из[VbaReferenceType](../../com.aspose.words/vbareferencetype) константы.
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
