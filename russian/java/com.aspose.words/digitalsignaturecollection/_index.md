---
title: DigitalSignatureCollection
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступную только для чтения коллекцию цифровых подписей, прикрепленных к документу.
type: docs
weight: 112
url: /ru/java/com.aspose.words/digitalsignaturecollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class DigitalSignatureCollection implements Iterable
```

Предоставляет доступную только для чтения коллекцию цифровых подписей, прикрепленных к документу.

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.

[Document.getDigitalSignatures()](../../com.aspose.words/document\#getDigitalSignatures--)
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает подпись документа по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [isValid()](#isValid--) | Возвращает значение true, если все цифровые подписи в этой коллекции действительны и документ не был изменен. Также возвращает значение true, если цифровые подписи отсутствуют. |
| [iterator()](#iterator--) | Возвращает объект итератора словаря, который можно использовать для перебора всех элементов в коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### get(int index) {#get-int-}
```
public DigitalSignature get(int index)
```


Получает подпись документа по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс подписи. |

**Возвращает:**
[DigitalSignature](../../com.aspose.words/digitalsignature) - Подпись документа по указанному индексу.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество элементов, содержащихся в коллекции.

**Возвращает:**
int - количество элементов, содержащихся в коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isValid() {#isValid--}
```
public boolean isValid()
```


Возвращает значение true, если все цифровые подписи в этой коллекции действительны и документ не был изменен. Также возвращает значение true, если цифровые подписи отсутствуют. Возвращает false, если хотя бы одна цифровая подпись недействительна.

**Возвращает:**
 логический -\{ true, если все цифровые подписи в этой коллекции действительны и документ не был подделан. Также возвращает true, если цифровых подписей нет.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект итератора словаря, который можно использовать для перебора всех элементов в коллекции.

**Возвращает:**
java.util.Iterator
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
