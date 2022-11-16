---
title: CustomXmlPropertyCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет набор настраиваемых XML-атрибутов или свойств смарт-тегов.
type: docs
weight: 107
url: /ru/java/com.aspose.words/customxmlpropertycollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class CustomXmlPropertyCollection implements Iterable
```

Представляет набор настраиваемых XML-атрибутов или свойств смарт-тегов.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

 Предметы[CustomXmlProperty](../../com.aspose.words/customxmlproperty) объекты.
## Методы

| Метод | Описание |
| --- | --- |
| [add(CustomXmlProperty property)](#add-com.aspose.words.CustomXmlProperty-) | Добавляет свойство в коллекцию. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [contains(String name)](#contains-java.lang.String-) | Определяет, содержит ли коллекция свойство с заданным именем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает свойство по указанному индексу. |
| [get(String name)](#get-java.lang.String-) | Предоставляет доступ к элементам коллекции. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | Возвращает отсчитываемый от нуля индекс указанного свойства в коллекции. |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | Удаляет свойство с указанным именем из коллекции. |
| [removeAt(int index)](#removeAt-int-) | Удаляет свойство по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(CustomXmlProperty property) {#add-com.aspose.words.CustomXmlProperty-}
```
public void add(CustomXmlProperty property)
```


Добавляет свойство в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| property | [CustomXmlProperty](../../com.aspose.words/customxmlproperty) | Добавляемое свойство. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Определяет, содержит ли коллекция свойство с заданным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | С учетом регистра имя свойства, которое необходимо найти. |

**Возвращает:**
boolean — Истинно, если элемент найден в коллекции; в противном случае ложно.
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
public CustomXmlProperty get(int index)
```


Получает свойство по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс свойства. |

**Возвращает:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty) - Свойство по указанному индексу.
### get(String name) {#get-java.lang.String-}
```
public CustomXmlProperty get(String name)
```


Предоставляет доступ к элементам коллекции. Получает свойство с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | С учетом регистра имя свойства, которое необходимо найти. |

**Возвращает:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty) - соответствующий[CustomXmlProperty](../../com.aspose.words/customxmlproperty) ценность.
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
### indexOfKey(String name) {#indexOfKey-java.lang.String-}
```
public int indexOfKey(String name)
```


Возвращает отсчитываемый от нуля индекс указанного свойства в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя свойства с учетом регистра. |

**Возвращает:**
int - индекс, основанный на нуле. Отрицательное значение, если не найдено.
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




### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Удаляет свойство с указанным именем из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя свойства с учетом регистра. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет свойство по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

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
