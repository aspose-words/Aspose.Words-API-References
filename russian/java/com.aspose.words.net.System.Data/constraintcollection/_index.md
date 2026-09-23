---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию ограничений для DataTable в Java."
type: docs
weight: 11
url: /ru/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Представляет коллекцию ограничений для [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Добавляет указанный объект [Constraint](../../com.aspose.words.net.system.data/constraint/) в коллекцию. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | Указывает, существует ли объект Constraint с указанным именем в коллекции. |
| [get(int index)](#get-int) | Получает [Constraint](../../com.aspose.words.net.system.data/constraint/) из коллекции по указанному индексу. |
| [get(String name)](#get-java.lang.String) | Получает [Constraint](../../com.aspose.words.net.system.data/constraint/) из коллекции по указанному имени. |
| [getCount()](#getCount) | Возвращает общее количество элементов в коллекции. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Удаляет указанный [Constraint](../../com.aspose.words.net.system.data/constraint/) из коллекции. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Добавляет указанный объект [Constraint](../../com.aspose.words.net.system.data/constraint/) в коллекцию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Constraint для добавления. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


Указывает, существует ли объект Constraint с указанным именем в коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Constraint для удаления. |

**Returns:**
boolean - true, если коллекция содержит указанный constraint; иначе false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Получает [Constraint](../../com.aspose.words.net.system.data/constraint/) из коллекции по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс constraint для возврата. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Получает [Constraint](../../com.aspose.words.net.system.data/constraint/) из коллекции по указанному имени.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Метод [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) ограничения для возврата. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Возвращает общее количество элементов в коллекции.

**Returns:**
int - Общее количество элементов в коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint}
```
public void remove(System.Data.Constraint constraint)
```


Удаляет указанный [Constraint](../../com.aspose.words.net.system.data/constraint/) из коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | [Constraint](../../com.aspose.words.net.system.data/constraint/) для удаления. |

