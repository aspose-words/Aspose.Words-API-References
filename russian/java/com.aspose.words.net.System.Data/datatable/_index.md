---
title: DataTable
second_title: Справочник по API Aspose.Words для Java
description: Представляет одну таблицу данных в памяти.
type: docs
weight: 25
url: /ru/java/com.aspose.words.net.system.data/datatable/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener)
```
public class DataTable implements System.Data.DataTableEventListener
```

Представляет одну таблицу данных в памяти.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataTable()](#DataTable--) |  Инициализирует новый экземпляр[DataTable](../../com.aspose.words.net.system.data/datatable) класс без аргументов. |
| [DataTable(String tableName)](#DataTable-java.lang.String-) |  Инициализирует новый экземпляр[DataTable](../../com.aspose.words.net.system.data/datatable) класс с указанным именем таблицы. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet-) | Создает объект путем упаковки указанного ResultSet. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String-) | Создает объект путем упаковки указанного ResultSet. |
## Методы

| Метод | Описание |
| --- | --- |
| [acceptChanges()](#acceptChanges--) | Фиксирует все изменения, внесенные в эту таблицу с момента последнего раза[acceptChanges()](../../com.aspose.words.net.system.data/datatable\#acceptChanges--) назывался. |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener-) |  |
| [clearEventListneers()](#clearEventListneers--) |  |
| [close()](#close--) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String-) | Проверить, существует ли данный столбец или нет |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getChildRelations()](#getChildRelations--) |  Получает коллекцию дочерних отношений для этого[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getClass()](#getClass--) |  |
| [getColumnName(int index)](#getColumnName-int-) | Аналог для .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns--) | Получает коллекцию столбцов, принадлежащих этой таблице. |
| [getColumnsCount()](#getColumnsCount--) |  |
| [getConstraints()](#getConstraints--) | Получает коллекцию ограничений, поддерживаемых этой таблицей. |
| [getDataSet()](#getDataSet--) |  Получает[DataSet](../../com.aspose.words.net.system.data/dataset) которому принадлежит эта таблица. |
| [getEnforceConstraints()](#getEnforceConstraints--) |  |
| [getNamespace()](#getNamespace--) |  Получает пространство имен для XML-представления данных, хранящихся в[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getParentRelations()](#getParentRelations--) |  Получает коллекцию родительских отношений для этого[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getPrimaryKey()](#getPrimaryKey--) | Получает массив столбцов, которые функционируют как первичные ключи для таблицы данных. |
| [getResultSet()](#getResultSet--) | Возвращает базовый объект Java ResultSet. |
| [getRows()](#getRows--) | Получает коллекцию строк, принадлежащих этой таблице. |
| [getTableName()](#getTableName--) |  Получает имя[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [hashCode()](#hashCode--) |  |
| [newRow()](#newRow--) |  Создает новый[DataRow](../../com.aspose.words.net.system.data/datarow) по той же схеме, что и таблица. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn-) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn-) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow-) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow-) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow-) |  |
| [refresh()](#refresh--) | Перезагружает все данные из ResultSet, если они есть. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean-) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String-) |  Задает пространство имен для XML-представления данных, хранящихся в[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn---) | Задает массив столбцов, которые функционируют как первичные ключи для таблицы данных. |
| [setTableName(String value)](#setTableName-java.lang.String-) |  Устанавливает имя[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataTable() {#DataTable--}
```
public DataTable()
```


 Инициализирует новый экземпляр[DataTable](../../com.aspose.words.net.system.data/datatable) класс без аргументов.

### DataTable(String tableName) {#DataTable-java.lang.String-}
```
public DataTable(String tableName)
```


 Инициализирует новый экземпляр[DataTable](../../com.aspose.words.net.system.data/datatable) класс с указанным именем таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | java.lang.String |  Имя для таблицы. Если tableName имеет значение null или пустую строку, имя по умолчанию дается при добавлении в[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet-}
```
public DataTable(ResultSet resultSet)
```


Создает объект путем упаковки указанного ResultSet. Пытается получить имя таблицы из метаданных первого столбца ResultSet.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | набор данных |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String-}
```
public DataTable(ResultSet resultSet, String tableName)
```


Создает объект путем упаковки указанного ResultSet.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | набор данных |
| tableName | java.lang.String | название таблицы |

### acceptChanges() {#acceptChanges--}
```
public void acceptChanges()
```


Фиксирует все изменения, внесенные в эту таблицу с момента последнего раза[acceptChanges()](../../com.aspose.words.net.system.data/datatable\#acceptChanges--) назывался.

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener-}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener) |  |

### clearEventListneers() {#clearEventListneers--}
```
public synchronized void clearEventListneers()
```




### close() {#close--}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String-}
```
public boolean containsColumn(String columnName)
```


Проверить, существует ли данный столбец или нет

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | имя столбца |

**Возвращает:**
 логический -`true` столбец можно найти по заданному`columnName`
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
### getChildRelations() {#getChildRelations--}
```
public System.Data.DataRelationCollection getChildRelations()
```


 Получает коллекцию дочерних отношений для этого[DataTable](../../com.aspose.words.net.system.data/datatable).

**Возвращает:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - А[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) который содержит дочерние отношения для таблицы. Пустая коллекция возвращается, если нет[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты существуют.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColumnName(int index) {#getColumnName-int-}
```
public String getColumnName(int index)
```


Аналог для .Net DataTable.Columns[i].ColumnName

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | \- индекс столбца |

**Возвращает:**
java.lang.String - имя столбца по его индексу.
### getColumns() {#getColumns--}
```
public System.Data.DataColumnCollection getColumns()
```


Получает коллекцию столбцов, принадлежащих этой таблице.

**Возвращает:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) - А[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) который содержит коллекцию[DataColumn](../../com.aspose.words.net.system.data/datacolumn) предметы для стола. Пустая коллекция возвращается, если нет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты существуют.
### getColumnsCount() {#getColumnsCount--}
```
public int getColumnsCount()
```




**Возвращает:**
int - количество столбцов
### getConstraints() {#getConstraints--}
```
public System.Data.ConstraintCollection getConstraints()
```


Получает коллекцию ограничений, поддерживаемых этой таблицей.

**Возвращает:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection) - А[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection) который содержит коллекцию[Constraint](../../com.aspose.words.net.system.data/constraint) предметы для стола. Пустая коллекция возвращается, если нет[Constraint](../../com.aspose.words.net.system.data/constraint) объекты существуют.
### getDataSet() {#getDataSet--}
```
public System.Data.DataSet getDataSet()
```


 Получает[DataSet](../../com.aspose.words.net.system.data/dataset) которому принадлежит эта таблица.

**Возвращает:**
[DataSet](../../com.aspose.words.net.system.data/dataset) -[DataSet](../../com.aspose.words.net.system.data/dataset) которому принадлежит эта таблица.
### getEnforceConstraints() {#getEnforceConstraints--}
```
public boolean getEnforceConstraints()
```




**Возвращает:**
boolean - флаг, указывающий, нарушается ли ограничение проверки или нет
### getNamespace() {#getNamespace--}
```
public String getNamespace()
```


 Получает пространство имен для XML-представления данных, хранящихся в[DataTable](../../com.aspose.words.net.system.data/datatable).

**Возвращает:**
 java.lang.String — пространство имен[DataTable](../../com.aspose.words.net.system.data/datatable).
### getParentRelations() {#getParentRelations--}
```
public System.Data.DataRelationCollection getParentRelations()
```


 Получает коллекцию родительских отношений для этого[DataTable](../../com.aspose.words.net.system.data/datatable).

**Возвращает:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - А[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) который содержит родительские отношения для таблицы. Пустая коллекция возвращается, если нет[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты существуют.
### getPrimaryKey() {#getPrimaryKey--}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Получает массив столбцов, которые функционируют как первичные ключи для таблицы данных.

**Возвращает:**
com.aspose.words.net.System.Data.DataColumn[ ] - Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.
### getResultSet() {#getResultSet--}
```
public ResultSet getResultSet()
```


Возвращает базовый объект Java ResultSet. В идеале мы хотели бы работать с DataTable в формате .Net. Но некоторые пользователи и даже некоторые наши образцы кода используют это свойство.

**Возвращает:**
java.sql.ResultSet — базовый java.sql.ResultSet
### getRows() {#getRows--}
```
public System.Data.DataRowCollection getRows()
```


Получает коллекцию строк, принадлежащих этой таблице.

**Возвращает:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) - А[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) который содержит[DataRow](../../com.aspose.words.net.system.data/datarow) объекты; в противном случае нулевое значение, если нет[DataRow](../../com.aspose.words.net.system.data/datarow) объекты существуют.
### getTableName() {#getTableName--}
```
public String getTableName()
```


 Получает имя[DataTable](../../com.aspose.words.net.system.data/datatable).

**Возвращает:**
 java.lang.String — Имя[DataTable](../../com.aspose.words.net.system.data/datatable).
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### newRow() {#newRow--}
```
public System.Data.DataRow newRow()
```


 Создает новый[DataRow](../../com.aspose.words.net.system.data/datarow) по той же схеме, что и таблица.

**Возвращает:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - А[DataRow](../../com.aspose.words.net.system.data/datarow) по той же схеме, что и[DataTable](../../com.aspose.words.net.system.data/datatable).
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn-}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn-}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow-}
```
public void onDataRowChanged(System.Data.DataRow row)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow-}
```
public void onDataRowDeleted(System.Data.DataRow row)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow-}
```
public void onDataRowInserted(System.Data.DataRow row)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### refresh() {#refresh--}
```
public void refresh()
```


Перезагружает все данные из ResultSet, если они есть.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean-}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| enforceConstraints | boolean | это флаг, который указывает, нарушается ли ограничение проверки или нет |

### setNamespace(String value) {#setNamespace-java.lang.String-}
```
public void setNamespace(String value)
```


 Задает пространство имен для XML-представления данных, хранящихся в[DataTable](../../com.aspose.words.net.system.data/datatable).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Пространство имен[DataTable](../../com.aspose.words.net.system.data/datatable). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn---}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Задает массив столбцов, которые функционируют как первичные ключи для таблицы данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |

### setTableName(String value) {#setTableName-java.lang.String-}
```
public void setTableName(String value)
```


 Устанавливает имя[DataTable](../../com.aspose.words.net.system.data/datatable).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Имя[DataTable](../../com.aspose.words.net.system.data/datatable). |

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
