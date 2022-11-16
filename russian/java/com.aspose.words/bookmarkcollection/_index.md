---
title: BookmarkCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов, представляющих закладки в указанном диапазоне.
type: docs
weight: 32
url: /ru/java/com.aspose.words/bookmarkcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class BookmarkCollection implements Iterable
```

 Коллекция[Bookmark](../../com.aspose.words/bookmark) объекты, представляющие закладки в указанном диапазоне.

 Чтобы узнать больше, посетите**Working with Bookmarks** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Удаляет все закладки из этой коллекции и из документа. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает закладку по указанному индексу. |
| [get(String bookmarkName)](#get-java.lang.String-) | Возвращает закладку по имени. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Возвращает количество закладок в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Bookmark bookmark)](#remove-com.aspose.words.Bookmark-) | Удаляет указанную закладку из документа. |
| [remove(String bookmarkName)](#remove-java.lang.String-) | Удаляет закладку с указанным именем. |
| [removeAt(int index)](#removeAt-int-) | Удаляет закладку по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


Удаляет все закладки из этой коллекции и из документа.

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
public Bookmark get(int index)
```


Возвращает закладку по указанному индексу.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

**Возвращает:**
[Bookmark](../../com.aspose.words/bookmark) Закладка по указанному индексу.
### get(String bookmarkName) {#get-java.lang.String-}
```
public Bookmark get(String bookmarkName)
```


Возвращает закладку по имени.

Возвращает null, если закладка с указанным именем не может быть найдена.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Нечувствительное к регистру имя закладки. |

**Возвращает:**
[Bookmark](../../com.aspose.words/bookmark) - Закладка по имени.
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


Возвращает количество закладок в коллекции.

**Возвращает:**
int — количество закладок в коллекции.
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




### remove(Bookmark bookmark) {#remove-com.aspose.words.Bookmark-}
```
public void remove(Bookmark bookmark)
```


Удаляет указанную закладку из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmark | [Bookmark](../../com.aspose.words/bookmark) | Закладка, которую нужно удалить. |

### remove(String bookmarkName) {#remove-java.lang.String-}
```
public void remove(String bookmarkName)
```


Удаляет закладку с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Нечувствительное к регистру имя удаляемой закладки. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет закладку по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс удаляемой закладки. |

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
