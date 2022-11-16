---
title: RevisionCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов, представляющих исправления в документе.
type: docs
weight: 484
url: /ru/java/com.aspose.words/revisioncollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class RevisionCollection implements Iterable
```

 Коллекция[Revision](../../com.aspose.words/revision) объекты, представляющие исправления в документе.

 Чтобы узнать больше, посетите**Track Changes in a Document** документальная статья.

Вы не создаете экземпляры этого класса напрямую. Использовать[Document.getRevisions()](../../com.aspose.words/document\#getRevisions--) свойство, чтобы получить ревизии, присутствующие в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [acceptAll()](#acceptAll--) | Принимает все изменения в этой коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает ревизию по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Возвращает количество ревизий в коллекции. |
| [getGroups()](#getGroups--) | Сбор ревизионных групп. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [rejectAll()](#rejectAll--) | Отклоняет все исправления в этой коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### acceptAll() {#acceptAll--}
```
public void acceptAll()
```


Принимает все изменения в этой коллекции.

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
public Revision get(int index)
```


Возвращает ревизию по указанному индексу.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

**Возвращает:**
[Revision](../../com.aspose.words/revision) - Ревизия по указанному индексу.
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


Возвращает количество ревизий в коллекции.

**Возвращает:**
int — количество ревизий в коллекции.
### getGroups() {#getGroups--}
```
public RevisionGroupCollection getGroups()
```


Сбор ревизионных групп.

**Возвращает:**
[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection) - соответствующий[RevisionGroupCollection](../../com.aspose.words/revisiongroupcollection) ценность.
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




### rejectAll() {#rejectAll--}
```
public void rejectAll()
```


Отклоняет все исправления в этой коллекции.

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
