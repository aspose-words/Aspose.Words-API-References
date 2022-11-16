---
title: BookmarksOutlineLevelCollection
second_title: Справочник по API Aspose.Words для Java
description: Набор уровней контура отдельных закладок.
type: docs
weight: 35
url: /ru/java/com.aspose.words/bookmarksoutlinelevelcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class BookmarksOutlineLevelCollection implements Iterable
```

Набор уровней контура отдельных закладок.

 Чтобы узнать больше, посетите**Working with Bookmarks** документальная статья.

Ключ — это строковое имя закладки без учета регистра. Значение представляет собой уровень структуры закладки int.

Уровень структуры закладки может быть значением от 0 до 9. Укажите 0, и закладка Word не будет отображаться в структуре документа. Укажите 1, и закладка Word будет отображаться в структуре документа на уровне 1; 2 для уровня 2 и так далее.
## Методы

| Метод | Описание |
| --- | --- |
| [add(String name, int outlineLevel)](#add-java.lang.String-int-) | Добавляет закладку в коллекцию. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [contains(String name)](#contains-java.lang.String-) | Определяет, содержит ли коллекция закладку с заданным именем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает уровень структуры закладки по указанному индексу. |
| [get(String name)](#get-java.lang.String-) | Предоставляет доступ к элементам коллекции. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | Возвращает отсчитываемый от нуля индекс указанной закладки в коллекции. |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | Удаляет закладку с указанным именем из коллекции. |
| [removeAt(int index)](#removeAt-int-) | Удаляет закладку по указанному индексу. |
| [set(int index, int value)](#set-int-int-) | Устанавливает уровень структуры закладки по указанному индексу. |
| [set(String name, int value)](#set-java.lang.String-int-) | Предоставляет доступ к элементам коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String name, int outlineLevel) {#add-java.lang.String-int-}
```
public void add(String name, int outlineLevel)
```


Добавляет закладку в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя добавляемой закладки. |
| outlineLevel | int | Уровень контура закладки. Допустимый диапазон от 0 до 9. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Определяет, содержит ли коллекция закладку с заданным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя закладки, которую необходимо найти. |

**Возвращает:**
boolean - Истинно, если элемент найден в коллекции; в противном случае ложно.
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
public int get(int index)
```


Получает уровень структуры закладки по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс закладки. |

**Возвращает:**
int — уровень структуры закладки. Допустимый диапазон от 0 до 9.
### get(String name) {#get-java.lang.String-}
```
public int get(String name)
```


Предоставляет доступ к элементам коллекции. Получает или задает уровень структуры закладки по имени закладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя закладки. |

**Возвращает:**
int — уровень структуры закладки. Допустимый диапазон от 0 до 9.
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


Возвращает отсчитываемый от нуля индекс указанной закладки в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя закладки. |

**Возвращает:**
int - индекс, основанный на нуле. Отрицательное значение, если не найдено.
### iterator() {#iterator--}
```
public Iterator iterator()
```




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


Удаляет закладку с указанным именем из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя закладки. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет закладку по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

### set(int index, int value) {#set-int-int-}
```
public void set(int index, int value)
```


Устанавливает уровень структуры закладки по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс закладки. |
| value | int | Уровень контура закладки. Допустимый диапазон от 0 до 9. |

### set(String name, int value) {#set-java.lang.String-int-}
```
public void set(String name, int value)
```


Предоставляет доступ к элементам коллекции. Получает или задает уровень структуры закладки по имени закладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя закладки. |
| value | int | Уровень контура закладки. Допустимый диапазон от 0 до 9. |

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
