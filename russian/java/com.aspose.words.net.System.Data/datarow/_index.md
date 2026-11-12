---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words для Java"
description: "Представляет строку данных в DataTable в Java."
type: docs
weight: 20
url: /ru/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Представляет строку данных в [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Методы

| Метод | Описание |
| --- | --- |
| [delete()](#delete) | Удаляет [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Получает данные, хранящиеся в указанном [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [get(int columnIndex)](#get-int) | Получает данные, хранящиеся в столбце, указанном по индексу. |
| [get(String columnName)](#get-java.lang.String) | Получает данные, хранящиеся в столбце, указанном по имени. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Получает дочерние строки этого [DataRow](../../com.aspose.words.net.system.data/datarow/) с использованием указанного [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getItemArray()](#getItemArray) | Получает все значения этой строки через массив. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Получает родительскую строку [DataRow](../../com.aspose.words.net.system.data/datarow/) с использованием указанного [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Получает родительские строки [DataRow](../../com.aspose.words.net.system.data/datarow/) с использованием указанного [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getRowState()](#getRowState) | Получает текущее состояние строки относительно её связи с [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [getTable()](#getTable) | Получает [DataTable](../../com.aspose.words.net.system.data/datatable/), для которой у этой строки есть схема. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | Читает значения из java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Устанавливает данные, хранящиеся в указанном [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | Устанавливает данные, хранящиеся в столбце, указанном по индексу. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | Устанавливает данные, хранящиеся в столбце, указанном по имени. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Устанавливает все значения этой строки через массив. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


Удаляет [DataRow](../../com.aspose.words.net.system.data/datarow/).

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Получает данные, хранящиеся в указанном [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), содержащий данные. |

**Returns:**
java.lang.Object — объект java.lang.Object, содержащий данные.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


Получает данные, хранящиеся в столбце, указанном по индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnIndex | int | Индекс столбца, начинающийся с нуля. |

**Returns:**
java.lang.Object — объект java.lang.Object, содержащий данные.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


Получает данные, хранящиеся в столбце, указанном по имени.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца. |

**Returns:**
java.lang.Object — объект java.lang.Object, содержащий данные.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Получает дочерние строки этого [DataRow](../../com.aspose.words.net.system.data/datarow/) с использованием указанного [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/), который следует использовать. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] — массив объектов [DataRow](../../com.aspose.words.net.system.data/datarow/) или массив нулевой длины.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Получает все значения этой строки через массив.

**Returns:**
java.lang.Object[] — массив типа java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Получает родительскую строку [DataRow](../../com.aspose.words.net.system.data/datarow/) с использованием указанного [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/), который следует использовать. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Получает родительские строки [DataRow](../../com.aspose.words.net.system.data/datarow/) с использованием указанного [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Объект [DataRelation](../../com.aspose.words.net.system.data/datarelation/), который следует использовать. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] — массив объектов [DataRow](../../com.aspose.words.net.system.data/datarow/) или массив нулевой длины.
### getRowState() {#getRowState}
```
public int getRowState()
```


Получает текущее состояние строки относительно её связи с [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Returns:**
int - Одно из значений [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) . Возвращаемое значение является побитовой комбинацией констант [DataRowState](../../com.aspose.words.net.system.data/datarowstate/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Получает [DataTable](../../com.aspose.words.net.system.data/datatable/), для которой у этой строки есть схема.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


Читает значения из java.sql.ResultSet

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | хранилище для чтения |

**Returns:**
boolean - true, если не произошло ошибок чтения
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Устанавливает данные, хранящиеся в указанном [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), содержащий данные. |
| значение | java.lang.Object | Объект java.lang.Object, содержащий данные. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


Устанавливает данные, хранящиеся в столбце, указанном по индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnIndex | int | Индекс столбца, начинающийся с нуля. |
| значение | java.lang.Object | Объект java.lang.Object, содержащий данные. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


Устанавливает данные, хранящиеся в столбце, указанном по имени.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца. |
| значение | java.lang.Object | Объект java.lang.Object, содержащий данные. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Устанавливает все значения этой строки через массив.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.Object[] | Массив типа java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String |  |
| данные | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| состояние | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
