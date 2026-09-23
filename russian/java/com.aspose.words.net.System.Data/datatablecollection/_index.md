---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию таблиц для DataSet в Java."
type: docs
weight: 26
url: /ru/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

Представляет коллекцию таблиц для [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Добавляет указанный DataTable в коллекцию. |
| [add(String name)](#add-java.lang.String) | Создаёт объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем и добавляет его в коллекцию. |
| [contains(String name)](#contains-java.lang.String) | Возвращает значение, указывающее, существует ли объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем в коллекции. |
| [get(int index)](#get-int) | Возвращает объект [DataTable](../../com.aspose.words.net.system.data/datatable/) по указанному индексу. |
| [get(String name)](#get-java.lang.String) | Возвращает объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Возвращает объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем в указанном пространстве имён. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Удаляет объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем из коллекции. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Добавляет указанный DataTable в коллекцию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Объект DataTable для добавления. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Создаёт объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем и добавляет его в коллекцию.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя, которое будет присвоено созданному объекту [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Возвращает значение, указывающее, существует ли объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем в коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя [DataTable](../../com.aspose.words.net.system.data/datatable/) для поиска. |

**Returns:**
boolean — true, если указанная таблица существует; иначе false.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Возвращает объект [DataTable](../../com.aspose.words.net.system.data/datatable/) по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Нулевой индекс [DataTable](../../com.aspose.words.net.system.data/datatable/) для поиска. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Возвращает объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя DataTable для поиска. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Возвращает объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем в указанном пространстве имён.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя DataTable для поиска. |
| tableNamespace | java.lang.String | Имя пространства имён [DataTable](../../com.aspose.words.net.system.data/datatable/), в котором следует искать. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int — общее количество элементов в этой коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


Удаляет объект [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем из коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя объекта [DataTable](../../com.aspose.words.net.system.data/datatable/) для удаления. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
