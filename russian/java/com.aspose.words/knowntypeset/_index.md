---
title: "KnownTypeSet"
linktitle: "KnownTypeSet"
second_title: "Aspose.Words для Java"
description: "Представляет неупорядоченный набор, т.е. в Java."
type: docs
weight: 412
url: /ru/java/com.aspose.words/knowntypeset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

Представляет неупорядоченный набор (т.е. коллекцию уникальных элементов), содержащий объекты java.lang.Class, полные или частичные имена которых могут использоваться в шаблонах отчетов для вызова статических членов соответствующих типов, выполнения приведения типов и т.д.

Чтобы узнать больше, посетите статью документации [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Методы

| Метод | Описание |
| --- | --- |
| [add(Class type)](#add-java.lang.Class) | Добавляет указанный объект java.lang.Class в набор. |
| [clear()](#clear) | Удаляет все элементы из набора. |
| [getCount()](#getCount) | Получает количество элементов в наборе. |
| [iterator()](#iterator) | Возвращает объект java.util.Iterator для перебора элементов набора. |
| [remove(Class type)](#remove-java.lang.Class) | Удаляет указанный объект java.lang.Class из набора. |
### add(Class type) {#add-java.lang.Class}
```
public void add(Class type)
```


Добавляет указанный объект java.lang.Class в набор.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| тип | java.lang.Class | Объект java.lang.Class для добавления. |

### clear() {#clear}
```
public void clear()
```


Удаляет все элементы из набора.

### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов в наборе.

**Returns:**
int — количество элементов в наборе.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект java.util.Iterator для перебора элементов набора.

**Returns:**
java.util.Iterator — объект java.util.Iterator для перебора элементов набора.
### remove(Class type) {#remove-java.lang.Class}
```
public void remove(Class type)
```


Удаляет указанный объект java.lang.Class из набора.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| тип | java.lang.Class | Объект java.lang.Class для удаления. |

