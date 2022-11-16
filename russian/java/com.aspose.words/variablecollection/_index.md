---
title: VariableCollection
second_title: Справочник по API Aspose.Words для Java
description: Набор переменных документа.
type: docs
weight: 592
url: /ru/java/com.aspose.words/variablecollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

Набор переменных документа.

 Чтобы узнать больше, посетите**Work with Document Properties** документальная статья.

Имена и значения переменных являются строками.

Имена переменных нечувствительны к регистру.
## Методы

| Метод | Описание |
| --- | --- |
| [add(String name, String value)](#add-java.lang.String-java.lang.String-) | Добавляет переменную документа в коллекцию. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [contains(String name)](#contains-java.lang.String-) | Определяет, содержит ли коллекция переменную документа с заданным именем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает переменную документа по указанному индексу. |
| [get(String name)](#get-java.lang.String-) | Предоставляет доступ к элементам коллекции. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | Возвращает отсчитываемый от нуля индекс указанной переменной документа в коллекции. |
| [iterator()](#iterator--) | Возвращает объект перечислителя, который можно использовать для перебора всех переменных в коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | Удаляет переменную документа с указанным именем из коллекции. |
| [removeAt(int index)](#removeAt-int-) | Удаляет переменную документа по указанному индексу. |
| [set(int index, String value)](#set-int-java.lang.String-) | Устанавливает переменную документа по указанному индексу. |
| [set(String name, String value)](#set-java.lang.String-java.lang.String-) | Предоставляет доступ к элементам коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String name, String value) {#add-java.lang.String-java.lang.String-}
```
public void add(String name, String value)
```


Добавляет переменную документа в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя добавляемой переменной. |
| value | java.lang.String | Значение переменной. Значение не может быть нулевым, если значение равно нулю, вместо него будет использоваться пустая строка. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Определяет, содержит ли коллекция переменную документа с заданным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя переменной документа, которую необходимо найти. |

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
public String get(int index)
```


Получает переменную документа по указанному индексу. Нулевые значения не допускаются в качестве правой части присваивания и будут заменены пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс переменной документа. |

**Возвращает:**
java.lang.String — переменная документа по указанному индексу.
### get(String name) {#get-java.lang.String-}
```
public String get(String name)
```


Предоставляет доступ к элементам коллекции. Получает или задает переменную документа по имени без учета регистра. Нулевые значения не допускаются в качестве правой части присваивания и будут заменены пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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


Возвращает отсчитываемый от нуля индекс указанной переменной документа в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя переменной. |

**Возвращает:**
int - индекс, основанный на нуле. Отрицательное значение, если не найдено.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект перечислителя, который можно использовать для перебора всех переменных в коллекции.

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


Удаляет переменную документа с указанным именем из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя переменной. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет переменную документа по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


Устанавливает переменную документа по указанному индексу. Нулевые значения не допускаются в качестве правой части присваивания и будут заменены пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс переменной документа. |
| value | java.lang.String | Переменная документа по указанному индексу. |

### set(String name, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String name, String value)
```


Предоставляет доступ к элементам коллекции. Получает или задает переменную документа по имени без учета регистра. Нулевые значения не допускаются в качестве правой части присваивания и будут заменены пустой строкой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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
