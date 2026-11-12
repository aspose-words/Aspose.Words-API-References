---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию объектов DataColumn для DataTable в Java."
type: docs
weight: 15
url: /ru/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Представляет коллекцию объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Создаёт и добавляет указанный объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName)](#add-java.lang.String) | Создаёт и добавляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) с указанным именем в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Создаёт и добавляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) с указанным именем и типом в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Создаёт и добавляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) с указанным именем, типом и конкретными значениями в коллекцию столбцов. |
| [clear()](#clear) | Очищает коллекцию от всех столбцов. |
| [contains(String name)](#contains-java.lang.String) | Проверяет, содержит ли коллекция столбец с указанным именем. |
| [get(int index)](#get-int) | Возвращает [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) из коллекции по указанному индексу. |
| [get(String name)](#get-java.lang.String) | Возвращает [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) из коллекции с указанным именем. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | Получает индекс столбца, указанного по имени. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Получает индекс столбца с указанным именем (имя не чувствительно к регистру). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Удаляет указанный объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) из коллекции. |
| [remove(String name)](#remove-java.lang.String) | Удаляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), имеющий указанное имя, из коллекции. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Создаёт и добавляет указанный объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для добавления. |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Создаёт и добавляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) с указанным именем в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Создаёт и добавляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) с указанным именем и типом в [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Методы [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String), используемые при создании столбца. |
| type | java.lang.Class | Методы [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) нового столбца. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Создаёт и добавляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) с указанным именем, типом и конкретными значениями в коллекцию столбцов.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | name |
| тип | java.lang.Class | тип данных |
| columnMapping | int | тип сопоставления столбцов |
| allowAutoIncrement | boolean | разрешён ли автоинкремент |
| allowDBNull | boolean | разрешено ли значение DBNull |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Очищает коллекцию от всех столбцов.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Проверяет, содержит ли коллекция столбец с указанным именем.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Методы [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) столбца, который нужно найти. |

**Returns:**
boolean — true, если столбец с таким именем существует; иначе false.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Возвращает [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) из коллекции по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс столбца, который нужно вернуть. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Возвращает [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) из коллекции с указанным именем.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Методы [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) столбца, который нужно вернуть. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int — общее количество элементов в коллекции.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


Получает индекс столбца, указанного по имени.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Имя столбца, который нужно вернуть. |

**Returns:**
int — индекс столбца, указанного по имени, если он найден; иначе -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Получает индекс столбца с указанным именем (имя не чувствительно к регистру).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца для поиска. |

**Returns:**
int — нулевой индекс столбца с указанным именем, или -1, если столбец не существует в коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Удаляет указанный объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) из коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для удаления. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Удаляет объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), имеющий указанное имя, из коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя столбца, который нужно удалить. |

