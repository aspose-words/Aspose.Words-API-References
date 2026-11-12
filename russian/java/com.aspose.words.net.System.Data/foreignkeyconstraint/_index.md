---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words для Java"
description: "Представляет ограничение действия, применяемое к набору столбцов в отношении первичного/внешнего ключа, когда значение или строка удаляется или обновляется в Java."
type: docs
weight: 29
url: /ru/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Представляет ограничение действия, применяемое к набору столбцов в отношении первичного/внешнего ключа, когда значение или строка удаляется или обновляется.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Инициализирует новый экземпляр класса [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) с указанным именем и массивами родительских и дочерних объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Инициализирует новый экземпляр класса [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) с указанными родительскими и дочерними объектами [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Инициализирует новый экземпляр класса [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) с указанным именем, родительскими и дочерними объектами [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Возвращает значение, указывающее, идентичен ли текущий [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) указанному объекту. |
| [getColumns()](#getColumns) | Возвращает дочерние столбцы этого ограничения. |
| [getConstraintName()](#getConstraintName) | Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | Возвращает действие, которое происходит в рамках этого ограничения при удалении строки. |
| [getRelatedColumns()](#getRelatedColumns) | Родительские столбцы этого ограничения. |
| [getRelatedTable()](#getRelatedTable) | Возвращает родительскую таблицу этого ограничения. |
| [getTable()](#getTable) | Возвращает дочернюю таблицу этого ограничения. |
| [getUpdateRule()](#getUpdateRule) | Возвращает действие, которое происходит в рамках этого ограничения при обновлении строки. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Инициализирует новый экземпляр класса [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) с указанным именем и массивами родительских и дочерних объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| constraintName | java.lang.String | Имя [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Если значение null или пустая строка, будет присвоено имя по умолчанию при добавлении в коллекцию ограничений. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив родительских [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в ограничении. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Массив дочерних [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в ограничении. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Инициализирует новый экземпляр класса [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) с указанными родительскими и дочерними объектами [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в ограничении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в ограничении. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Инициализирует новый экземпляр класса [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) с указанным именем, родительскими и дочерними объектами [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| constraintName | java.lang.String | Имя ограничения. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Родительский [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в ограничении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Дочерний [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) в ограничении. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Возвращает значение, указывающее, идентичен ли текущий [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) указанному объекту.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| key | java.lang.Object | Объект, с которым сравнивается данный [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Два [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) равны, если они ограничивают одни и те же столбцы. |

**Returns:**
boolean - true, если объекты идентичны; иначе false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Возвращает дочерние столбцы этого ограничения.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) , являющихся дочерними столбцами ограничения.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String — Имя [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Возвращает действие, которое происходит в рамках этого ограничения при удалении строки.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Родительские столбцы этого ограничения.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - массив объектов [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) , являющихся родительскими столбцами ограничения.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Возвращает родительскую таблицу этого ограничения.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Возвращает дочернюю таблицу этого ограничения.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Возвращает действие, которое происходит в рамках этого ограничения при обновлении строки.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


Имя ограничения в [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя [Constraint](../../com.aspose.words.net.system.data/constraint/). |

