---
title: CustomPartCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию объектов.
type: docs
weight: 103
url: /ru/java/com.aspose.words/custompartcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class CustomPartCollection implements Iterable
```

 Представляет собой совокупность[CustomPart](../../com.aspose.words/custompart) объекты.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

 Обычно вам не нужно создавать экземпляры этого класса. Вы получаете доступ к пользовательским частям, связанным с пакетом OOXML, через[Document.getPackageCustomParts()](../../com.aspose.words/document\#getPackageCustomParts--) / [Document.setPackageCustomParts(com.aspose.words.CustomPartCollection)](../../com.aspose.words/document\#setPackageCustomParts-com.aspose.words.CustomPartCollection-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [add(CustomPart part)](#add-com.aspose.words.CustomPart-) | Добавляет элемент в коллекцию. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [deepClone()](#deepClone--) | Создает глубокую копию этой коллекции и ее элементов. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает элемент по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | Удаляет элемент по указанному индексу. |
| [set(int index, CustomPart value)](#set-int-com.aspose.words.CustomPart-) | Устанавливает элемент по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(CustomPart part) {#add-com.aspose.words.CustomPart-}
```
public void add(CustomPart part)
```


Добавляет элемент в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| part | [CustomPart](../../com.aspose.words/custompart) | Элемент для добавления. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### deepClone() {#deepClone--}
```
public CustomPartCollection deepClone()
```


Создает глубокую копию этой коллекции и ее элементов.

**Возвращает:**
[CustomPartCollection](../../com.aspose.words/custompartcollection)
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
public CustomPart get(int index)
```


Получает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс элемента. |

**Возвращает:**
[CustomPart](../../com.aspose.words/custompart) - Элемент по указанному индексу.
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
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции.

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




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

### set(int index, CustomPart value) {#set-int-com.aspose.words.CustomPart-}
```
public void set(int index, CustomPart value)
```


Устанавливает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс элемента. |
| value | [CustomPart](../../com.aspose.words/custompart) | Элемент по указанному индексу. |

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
