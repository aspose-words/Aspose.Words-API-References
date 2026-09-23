---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию объектов DataRelation для этого DataSet в Java."
type: docs
weight: 19
url: /ru/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Представляет коллекцию объектов [DataRelation](../../com.aspose.words.net.system.data/datarelation/) для этого [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Создаёт [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с указанными родительским и дочерним столбцами и добавляет его в коллекцию. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Добавляет [DataRelation](../../com.aspose.words.net.system.data/datarelation/) в [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Добавляет отношение в коллекцию. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Добавляет отношение в коллекцию. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Создаёт [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с указанным именем, а также родительскими и дочерними столбцами и добавляет его в коллекцию. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Создаёт [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с указанным именем, родительскими и дочерними столбцами, с необязательными ограничениями в соответствии со значением параметра  createConstraints , и добавляет его в коллекцию. |
| [clear()](#clear) | Очищает коллекцию от всех отношений. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Проверяет, существует ли DataRelation с указанным именем (без учёта регистра) в коллекции. |
| [get(int index)](#get-int) | Получает объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/) по указанному индексу. |
| [get(String name)](#get-java.lang.String) | Получает объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/), указанный по имени. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Получает индекс указанного объекта [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Удаляет отношение по указанному индексу из коллекции. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Создаёт [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с указанными родительским и дочерним столбцами и добавляет его в коллекцию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский столбец отношения. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний столбец отношения. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Добавляет [DataRelation](../../com.aspose.words.net.system.data/datarelation/) в [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | DataRelation для добавления в коллекцию. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Добавляет отношение в коллекцию. Не выполняет проверку на дублирование и т.п.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Родительская таблица отношения. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Дочерняя таблица отношения. |
| parentColumnName | java.lang.String | Имя родительского столбца отношения. |
| childColumnName | java.lang.String | Имя дочернего столбца отношения. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Добавляет отношение в коллекцию. Не выполняет проверку на дублирование и т.п.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Родительская таблица отношения. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Дочерняя таблица отношения. |
| parentColumnNames | java.lang.String[] | Массив имен родительских столбцов отношения. |
| childColumnNames | java.lang.String[] | Массив имен дочерних столбцов отношения. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Создаёт [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с указанным именем, а также родительскими и дочерними столбцами и добавляет его в коллекцию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя отношения. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский столбец отношения. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний столбец отношения. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Создаёт [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с указанным именем, родительскими и дочерними столбцами, с необязательными ограничениями в соответствии со значением параметра  createConstraints , и добавляет его в коллекцию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя отношения. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский столбец отношения. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний столбец отношения. |
| createConstraints | boolean | true — создать ограничения; иначе false. (По умолчанию true). |

### clear() {#clear}
```
public void clear()
```


Очищает коллекцию от всех отношений.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Проверяет, существует ли DataRelation с указанным именем (без учёта регистра) в коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Имя отношения для поиска. |

**Returns:**
boolean — true, если отношение с указанным именем существует; иначе false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Получает объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/) по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс для поиска. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


Получает объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/), указанный по имени.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя отношения для поиска. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int — общее количество элементов в коллекции
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Получает индекс указанного объекта [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Отношение для поиска. |

**Returns:**
int — нулевой индекс отношения или -1, если отношение не найдено в коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет отношение по указанному индексу из коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс отношения для удаления. |

