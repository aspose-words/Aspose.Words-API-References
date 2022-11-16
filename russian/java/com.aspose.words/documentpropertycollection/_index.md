---
title: DocumentPropertyCollection
second_title: Справочник по API Aspose.Words для Java
description: Базовый класс для и коллекций.
type: docs
weight: 127
url: /ru/java/com.aspose.words/documentpropertycollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public abstract class DocumentPropertyCollection implements Iterable
```

 Базовый класс для[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) а также[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) коллекции.

 Чтобы узнать больше, посетите**Work with Document Properties** документальная статья.

Имена свойств нечувствительны к регистру.

Свойства в коллекции отсортированы в алфавитном порядке по имени.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DocumentPropertyCollection()](#DocumentPropertyCollection--) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Удаляет все свойства из коллекции. |
| [contains(String name)](#contains-java.lang.String-) | Возвращает true, если свойство с указанным именем существует в коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект по индексу. |
| [get(String name)](#get-java.lang.String-) | Предоставляет доступ к элементам коллекции. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов в коллекции. |
| [hashCode()](#hashCode--) |  |
| [indexOf(String name)](#indexOf-java.lang.String-) | Получает индекс свойства по имени. |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | Удаляет свойство с указанным именем из коллекции. |
| [removeAt(int index)](#removeAt-int-) | Удаляет свойство по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DocumentPropertyCollection() {#DocumentPropertyCollection--}
```
public DocumentPropertyCollection()
```


### clear() {#clear--}
```
public void clear()
```


Удаляет все свойства из коллекции.

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Возвращает true, если свойство с указанным именем существует в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя свойства. |

**Возвращает:**
boolean — Истинно, если свойство существует в коллекции; ложно в противном случае.
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
public DocumentProperty get(int index)
```


 Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект по индексу.

**Note:** В Java этот метод медленный, потому что перебирает все узлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  Отсчитываемый от нуля индекс[DocumentProperty](../../com.aspose.words/documentproperty) получить. |

**Возвращает:**
[DocumentProperty](../../com.aspose.words/documentproperty) - А[DocumentProperty](../../com.aspose.words/documentproperty) объект по индексу.
### get(String name) {#get-java.lang.String-}
```
public DocumentProperty get(String name)
```


 Предоставляет доступ к элементам коллекции. Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект по имени свойства.

Возвращает null, если свойство с указанным именем не найдено.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя извлекаемого свойства. |

**Возвращает:**
[DocumentProperty](../../com.aspose.words/documentproperty) - соответствующий[DocumentProperty](../../com.aspose.words/documentproperty) ценность.
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


Получает количество элементов в коллекции.

**Возвращает:**
int - количество элементов в коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### indexOf(String name) {#indexOf-java.lang.String-}
```
public int indexOf(String name)
```


Получает индекс свойства по имени.

**Note:** В Java этот метод медленный, потому что перебирает все узлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя свойства. |

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
| name | java.lang.String | Нечувствительное к регистру имя свойства. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет свойство по указанному индексу.

**Note:** В Java этот метод медленный, потому что перебирает все узлы.

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
