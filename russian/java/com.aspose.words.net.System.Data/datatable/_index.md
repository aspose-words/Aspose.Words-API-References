---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words для Java"
description: "Представляет одну таблицу данных в памяти в Java."
type: docs
weight: 25
url: /ru/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

Представляет одну таблицу данных в памяти.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataTable()](#DataTable) | Инициализирует новый экземпляр класса [DataTable](../../com.aspose.words.net.system.data/datatable/) без аргументов. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Инициализирует новый экземпляр класса [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем таблицы. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Создаёт объект, оборачивая указанный ResultSet. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Создаёт объект, оборачивая указанный ResultSet. |
## Методы

| Метод | Описание |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Фиксирует все изменения, внесённые в эту таблицу с момента последнего вызова [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges). |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Проверьте, существует ли указанный столбец. |
| [getChildRelations()](#getChildRelations) | Получает коллекцию дочерних связей для этой [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnName(int index)](#getColumnName-int) | Аналог для .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | Получает коллекцию столбцов, принадлежащих этой таблице. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Получает коллекцию ограничений, поддерживаемых этой таблицей. |
| [getDataSet()](#getDataSet) | Получает [DataSet](../../com.aspose.words.net.system.data/dataset/), к которому принадлежит эта таблица. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | Получает пространство имён для XML-представления данных, хранящихся в [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getParentRelations()](#getParentRelations) | Получает коллекцию родительских связей для этой [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getPrimaryKey()](#getPrimaryKey) | Получает массив столбцов, которые выступают в качестве первичных ключей для таблицы данных. |
| [getResultSet()](#getResultSet) | Возвращает базовый объект Java ResultSet. |
| [getRows()](#getRows) | Получает коллекцию строк, принадлежащих этой таблице. |
| [getTableName()](#getTableName) | Получает имя [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [newRow()](#newRow) | Создаёт новый [DataRow](../../com.aspose.words.net.system.data/datarow/) с той же схемой, что и таблица. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | Перезагружает все данные из ResultSet, если он присутствует. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Устанавливает пространство имён для XML-представления данных, хранящихся в [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Устанавливает массив столбцов, которые выступают в качестве первичных ключей для таблицы данных. |
| [setTableName(String value)](#setTableName-java.lang.String) | Устанавливает имя [DataTable](../../com.aspose.words.net.system.data/datatable/). |
### DataTable() {#DataTable}
```
public DataTable()
```


Инициализирует новый экземпляр класса [DataTable](../../com.aspose.words.net.system.data/datatable/) без аргументов.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Инициализирует новый экземпляр класса [DataTable](../../com.aspose.words.net.system.data/datatable/) с указанным именем таблицы.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | java.lang.String | Имя, которое будет присвоено таблице. Если  tableName  равен null или пустой строке, при добавлении в [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) будет использовано имя по умолчанию. |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Создаёт объект, оборачивая указанный ResultSet. Пытается получить имя таблицы из метаданных первого столбца ResultSet.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | набор данных |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Создаёт объект, оборачивая указанный ResultSet.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | набор данных |
| tableName | java.lang.String | имя таблицы |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Фиксирует все изменения, внесённые в эту таблицу с момента последнего вызова [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges).

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/) |  |

### clearEventListneers() {#clearEventListneers}
```
public synchronized void clearEventListneers()
```




### close() {#close}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String}
```
public boolean containsColumn(String columnName)
```


Проверьте, существует ли указанный столбец.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | имя столбца |

**Returns:**
boolean - `true`, если столбец может быть найден по заданному `columnName`
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Получает коллекцию дочерних связей для этой [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


Аналог для .Net DataTable.Columns[i].ColumnName

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | - индекс столбца |

**Returns:**
java.lang.String - имя столбца по его индексу.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Получает коллекцию столбцов, принадлежащих этой таблице.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - количество столбцов
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Получает коллекцию ограничений, поддерживаемых этой таблицей.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Получает [DataSet](../../com.aspose.words.net.system.data/dataset/), к которому принадлежит эта таблица.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - флаг, указывающий, нарушено ли ограничение проверки
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Получает пространство имён для XML-представления данных, хранящихся в [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Пространство имён [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Получает коллекцию родительских связей для этой [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Получает массив столбцов, которые выступают в качестве первичных ключей для таблицы данных.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Возвращает базовый объект Java ResultSet. В идеале мы хотели бы работать с DataTable в стиле .Net. Но некоторые пользователи и даже некоторые наши примеры кода используют это свойство.

**Returns:**
java.sql.ResultSet - базовый java.sql.ResultSet
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Получает коллекцию строк, принадлежащих этой таблице.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


Получает имя [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Имя [DataTable](../../com.aspose.words.net.system.data/datatable/).
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Создаёт новый [DataRow](../../com.aspose.words.net.system.data/datarow/) с той же схемой, что и таблица.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


Обновить слушатель при удалении DataColumn

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


Обновить слушатель при вставке DataColumn

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


Обновить слушатель при изменении DataRow

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


Обновить слушатель при удалении DataRow

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


Обновить слушатель при вставке DataRow

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


Перезагружает все данные из ResultSet, если он присутствует.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| enforceConstraints | boolean | это флаг, указывающий, нарушено ли ограничение проверки |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Устанавливает пространство имён для XML-представления данных, хранящихся в [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Пространство имён [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Устанавливает массив столбцов, которые выступают в качестве первичных ключей для таблицы данных.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Устанавливает имя [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя [DataTable](../../com.aspose.words.net.system.data/datatable/). |

