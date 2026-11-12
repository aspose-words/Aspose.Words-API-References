---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words для Java"
description: "Представляет отношение «родитель/дочерний» между двумя объектами DataTable в Java."
type: docs
weight: 18
url: /ru/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

Представляет отношение «родитель/дочерний» между двумя объектами [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени, таблиц‑родителя и‑дочери, соответствующих массивов столбцов родителя и дочери. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени, соответствующих массивов объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) родителя и дочери, а также значения, указывающего, следует ли создавать ограничения. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени, объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) родителя и дочери, а также значения, указывающего, следует ли создавать ограничения. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени [DataRelation](../../com.aspose.words.net.system.data/datarelation/), а также объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) родителя и дочери. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | Возвращает дочерние объекты [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) этой связи. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | Возвращает [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) для этой связи. |
| [getChildTable()](#getChildTable) | Возвращает дочернюю таблицу этой связи. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | Возвращает [DataSet](../../com.aspose.words.net.system.data/dataset/), к которому принадлежит [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | Возвращает массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), являющихся столбцами‑родителями этой [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | Возвращает [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/), гарантирующий уникальность значений в столбце‑родителе [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentTable()](#getParentTable) | Возвращает родительскую [DataTable](../../com.aspose.words.net.system.data/datatable/) этой [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | Возвращает имя, используемое для получения [DataRelation](../../com.aspose.words.net.system.data/datarelation/) из [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | Устанавливает значение, указывающее, являются ли объекты [DataRelation](../../com.aspose.words.net.system.data/datarelation/) вложенными. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени, таблиц‑родителя и‑дочери, соответствующих массивов столбцов родителя и дочери.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String | Имя DataRelation. Если значение null или пустая строка (\"\"), при добавлении созданного объекта в DataRelationCollection будет присвоено имя по умолчанию. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Родительская таблица в отношении. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Дочерняя таблица в отношении. |
| parentColumnNames | java.lang.String[] | Имя родительского DataColumn в отношении. |
| childColumnNames | java.lang.String[] | Дочерние DataColumn в отношении. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени, соответствующих массивов объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) родителя и дочери, а также значения, указывающего, следует ли создавать ограничения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String | Имя отношения. Если null или пустая строка (""), будет присвоено имя по умолчанию, когда созданный объект будет добавлен в [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив родительских [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) объектов. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив дочерних [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) объектов. |
| createConstraints | boolean | Значение, указывающее, следует ли создавать ограничения. true, если ограничения созданы. В противном случае false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени, объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) родителя и дочери, а также значения, указывающего, следует ли создавать ограничения.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String | Имя отношения. Если null или пустая строка (""), будет присвоено имя по умолчанию, когда созданный объект будет добавлен в [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в отношении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в отношении. |
| createConstraints | boolean | Значение, указывающее, созданы ли ограничения. true, если ограничения созданы. В противном случае false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Инициализирует новый экземпляр класса [DataRelation](../../com.aspose.words.net.system.data/datarelation/) с использованием указанного имени [DataRelation](../../com.aspose.words.net.system.data/datarelation/), а также объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) родителя и дочери.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String | Имя [DataRelation](../../com.aspose.words.net.system.data/datarelation/). Если null или пустая строка (""), будет присвоено имя по умолчанию, когда созданный объект будет добавлен в [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в отношении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в отношении. |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] — имена дочерних DataColumn этого отношения.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


Возвращает дочерние объекты [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) этой связи.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getChildKey() {#getChildKey}
```
public System.Data.DataKey getChildKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getChildKeyConstraint() {#getChildKeyConstraint}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


Возвращает [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) для этой связи.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


Возвращает дочернюю таблицу этой связи.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String — имя дочерней DataTable этого DataRelation.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Возвращает [DataSet](../../com.aspose.words.net.system.data/dataset/), к которому принадлежит [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] — имена родительских DataColumn этого отношения.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


Возвращает массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), являющихся столбцами‑родителями этой [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] — массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/), которые являются родительскими колонками этого [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### getParentKey() {#getParentKey}
```
public System.Data.DataKey getParentKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getParentKeyConstraint() {#getParentKeyConstraint}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


Возвращает [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/), гарантирующий уникальность значений в столбце‑родителе [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


Возвращает родительскую [DataTable](../../com.aspose.words.net.system.data/datatable/) этой [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String — имя родительской DataTable этого DataRelation.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


Возвращает имя, используемое для получения [DataRelation](../../com.aspose.words.net.system.data/datarelation/) из [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Returns:**
java.lang.String — имя [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


Устанавливает значение, указывающее, являются ли объекты [DataRelation](../../com.aspose.words.net.system.data/datarelation/) вложенными.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | true, если объекты [DataRelation](../../com.aspose.words.net.system.data/datarelation/) вложены; в противном случае false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

