---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words для Java"
description: "Представляет ограничение набора столбцов, в котором все значения должны быть уникальными в Java."
type: docs
weight: 32
url: /ru/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

Представляет ограничение набора столбцов, в котором все значения должны быть уникальными.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с указанным именем, массивом объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения и значением, указывающим, является ли ограничение первичным ключом. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с массивом объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения и значением, указывающим, является ли ограничение первичным ключом. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с указанным массивом объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с указанным [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | Сравнивает это ограничение со вторым, чтобы определить, идентичны ли они. |
| [getColumns()](#getColumns) | Возвращает массив столбцов, на которые влияет это ограничение. |
| [getConstraintName()](#getConstraintName) | Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getTable()](#getTable) | Возвращает таблицу, к которой относится это ограничение. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | Возвращает значение, указывающее, является ли ограничение первичным ключом. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с указанным именем, массивом объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения и значением, указывающим, является ли ограничение первичным ключом.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя ограничения. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения. |
| isPrimaryKey | boolean | true, чтобы указать, что ограничение является первичным ключом; иначе false. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с массивом объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения и значением, указывающим, является ли ограничение первичным ключом.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения. |
| isPrimaryKey | boolean | true, чтобы указать, что ограничение является первичным ключом; иначе false. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с указанным массивом объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Инициализирует новый экземпляр класса [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) с указанным [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Объект [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) для ограничения. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


Сравнивает это ограничение со вторым, чтобы определить, идентичны ли они.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| key2 | java.lang.Object | Объект, с которым сравнивается данный [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/). |

**Returns:**
boolean - true, если ограничения равны; иначе false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Возвращает массив столбцов, на которые влияет это ограничение.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String — Имя [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Возвращает таблицу, к которой относится это ограничение.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the constraint belongs.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isPrimaryKey() {#isPrimaryKey}
```
public boolean isPrimaryKey()
```


Возвращает значение, указывающее, является ли ограничение первичным ключом.

**Returns:**
boolean - true, если ограничение находится на первичном ключе; иначе false.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя [Constraint](../../com.aspose.words.net.system.data/constraint/). |

