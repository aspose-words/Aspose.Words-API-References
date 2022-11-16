---
title: ConstraintCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет набор ограничений для .
type: docs
weight: 11
url: /ru/java/com.aspose.words.net.system.data/constraintcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

 Представляет набор ограничений для[DataTable](../../com.aspose.words.net.system.data/datatable).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint-) |  Добавляет указанный[Constraint](../../com.aspose.words.net.system.data/constraint) возражать против коллекции. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint-) | Указывает, существует ли в коллекции объект Constraint, указанный по имени. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Получает[Constraint](../../com.aspose.words.net.system.data/constraint) из коллекции по указанному индексу. |
| [get(String name)](#get-java.lang.String-) |  Получает[Constraint](../../com.aspose.words.net.system.data/constraint) из коллекции с указанным именем. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает общее количество элементов в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint-) |  Удаляет указанный[Constraint](../../com.aspose.words.net.system.data/constraint) из коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint-}
```
public void add(System.Data.Constraint constraint)
```


 Добавляет указанный[Constraint](../../com.aspose.words.net.system.data/constraint) возражать против коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint) | Ограничение для добавления. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint-}
```
public boolean contains(System.Data.Constraint cc)
```


Указывает, существует ли в коллекции объект Constraint, указанный по имени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint) | Ограничение, которое нужно удалить. |

**Возвращает:**
boolean — true, если коллекция содержит указанное ограничение; в противном случае ложно.
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
public System.Data.Constraint get(int index)
```


 Получает[Constraint](../../com.aspose.words.net.system.data/constraint) из коллекции по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс возвращаемого ограничения. |

**Возвращает:**
[Constraint](../../com.aspose.words.net.system.data/constraint) -[Constraint](../../com.aspose.words.net.system.data/constraint) по указанному индексу.
### get(String name) {#get-java.lang.String-}
```
public System.Data.Constraint get(String name)
```


 Получает[Constraint](../../com.aspose.words.net.system.data/constraint) из коллекции с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint\#getConstraintName--) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint\#setConstraintName-java.lang.String-) ограничения на возврат. |

**Возвращает:**
[Constraint](../../com.aspose.words.net.system.data/constraint) -[Constraint](../../com.aspose.words.net.system.data/constraint) с указанным именем; в противном случае нулевое значение, если[Constraint](../../com.aspose.words.net.system.data/constraint) не существует.
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


Получает общее количество элементов в коллекции.

**Возвращает:**
int — общее количество элементов в коллекции.
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




### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint-}
```
public void remove(System.Data.Constraint constraint)
```


 Удаляет указанный[Constraint](../../com.aspose.words.net.system.data/constraint) из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint) | [Constraint](../../com.aspose.words.net.system.data/constraint) удалять. |

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
