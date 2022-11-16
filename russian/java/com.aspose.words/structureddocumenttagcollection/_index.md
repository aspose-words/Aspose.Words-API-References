---
title: StructuredDocumentTagCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция экземпляров, представляющих теги структурированного документа в указанном диапазоне.
type: docs
weight: 533
url: /ru/java/com.aspose.words/structureddocumenttagcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class StructuredDocumentTagCollection implements Iterable
```

 Коллекция[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag) экземпляры, представляющие теги структурированного документа в указанном диапазоне.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает тег структурированного документа по указанному индексу. |
| [getById(int id)](#getById-int-) | Возвращает тег структурированного документа по идентификатору. |
| [getByTag(String tag)](#getByTag-java.lang.String-) | Возвращает первый тег структурированного документа, обнаруженный в коллекции с указанным тегом. |
| [getByTitle(String title)](#getByTitle-java.lang.String-) | Возвращает первый найденный в коллекции тег структурированного документа с указанным заголовком. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Возвращает количество тегов структурированного документа в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(int id)](#remove-int-) | Удаляет тег структурированного документа с указанным идентификатором. |
| [removeAt(int index)](#removeAt-int-) | Удаляет тег структурированного документа по указанному индексу. |
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
public IStructuredDocumentTag get(int index)
```


Возвращает тег структурированного документа по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

**Возвращает:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag) - Тег структурированного документа по указанному индексу.
### getById(int id) {#getById-int-}
```
public IStructuredDocumentTag getById(int id)
```


Возвращает тег структурированного документа по идентификатору.

Возвращает null, если тег структурированного документа с указанным идентификатором не может быть найден.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | int | Идентификатор тега структурированного документа. |

**Возвращает:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### getByTag(String tag) {#getByTag-java.lang.String-}
```
public IStructuredDocumentTag getByTag(String tag)
```


Возвращает первый тег структурированного документа, обнаруженный в коллекции с указанным тегом.

Возвращает null, если тег структурированного документа с указанным тегом не может быть найден.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tag | java.lang.String | Тег тега структурированного документа. |

**Возвращает:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
### getByTitle(String title) {#getByTitle-java.lang.String-}
```
public IStructuredDocumentTag getByTitle(String title)
```


Возвращает первый найденный в коллекции тег структурированного документа с указанным заголовком.

Возвращает значение null, если тег структурированного документа с указанным заголовком не найден.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| title | java.lang.String | Тег заголовка структурированного документа. |

**Возвращает:**
[IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
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


Возвращает количество тегов структурированного документа в коллекции.

**Возвращает:**
int — количество тегов структурированного документа в коллекции.
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




### remove(int id) {#remove-int-}
```
public void remove(int id)
```


Удаляет тег структурированного документа с указанным идентификатором.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | int | Идентификатор тега структурированного документа. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет тег структурированного документа по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

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
