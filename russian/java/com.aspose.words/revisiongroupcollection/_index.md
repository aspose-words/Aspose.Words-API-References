---
title: RevisionGroupCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов, представляющих группы редакций в документе.
type: docs
weight: 487
url: /ru/java/com.aspose.words/revisiongroupcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class RevisionGroupCollection implements Iterable
```

 Коллекция[RevisionGroup](../../com.aspose.words/revisiongroup) объекты, которые представляют группы ревизий в документе.

 Чтобы узнать больше, посетите**Track Changes in a Document** документальная статья.

Вы не создаете экземпляры этого класса напрямую. Использовать[RevisionCollection.getGroups()](../../com.aspose.words/revisioncollection\#getGroups--) свойство, чтобы группы ревизий присутствовали в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает группу ревизий по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Возвращает количество групп ревизий в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
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
public RevisionGroup get(int index)
```


Возвращает группу ревизий по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |

**Возвращает:**
[RevisionGroup](../../com.aspose.words/revisiongroup) - Группа ревизий по указанному индексу.
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


Возвращает количество групп ревизий в коллекции.

**Возвращает:**
int — количество групп ревизий в коллекции.
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


Возвращает объект перечислителя.

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
