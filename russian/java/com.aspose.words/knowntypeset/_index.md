---
title: KnownTypeSet
second_title: Справочник по API Aspose.Words для Java
description: Представляет неупорядоченный набор, т.е.
type: docs
weight: 356
url: /ru/java/com.aspose.words/knowntypeset/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

Представляет неупорядоченный набор (т. е. набор уникальных элементов), содержащий объекты java.lang.Class, полные или частично определенные имена которых можно использовать в шаблонах отчетов для вызова статических членов соответствующих типов, выполнения приведения типов и т. д.

 Чтобы узнать больше, посетите**LINQ Reporting Engine** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [add(Class type)](#add-java.lang.Class-) | Добавляет в набор указанный объект java.lang.Class. |
| [clear()](#clear--) | Удаляет все элементы из набора. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов в наборе. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект java.util.Iterator для перебора элементов набора. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Class type)](#remove-java.lang.Class-) | Удаляет указанный объект java.lang.Class из набора. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(Class type) {#add-java.lang.Class-}
```
public void add(Class type)
```


Добавляет в набор указанный объект java.lang.Class. Выдает java.lang.IllegalArgumentException в следующих случаях:

\- тип нулевой.

\- type представляет тип void.

\- type представляет невидимый тип, т. е. непубличный тип или общедоступный вложенный тип, который имеет непубличный внешний тип.

\- type представляет тип массива.

\- тип уже добавлен в набор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | java.lang.Class | Добавляемый объект java.lang.Class. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из набора.

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


Получает количество элементов в наборе.

**Возвращает:**
int - Количество элементов в наборе.
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


Возвращает объект java.util.Iterator для перебора элементов набора.

**Возвращает:**
java.util.Iterator — объект java.util.Iterator для перебора элементов набора.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(Class type) {#remove-java.lang.Class-}
```
public void remove(Class type)
```


Удаляет указанный объект java.lang.Class из набора. Выдает java.lang.IllegalArgumentException, если тип равен null.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| type | java.lang.Class | Объект java.lang.Class для удаления. |

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
