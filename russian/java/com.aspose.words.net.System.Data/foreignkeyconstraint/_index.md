---
title: ForeignKeyConstraint
second_title: Справочник по API Aspose.Words для Java
description: Представляет ограничение действия, применяемое к набору столбцов в отношении первичного/внешнего ключа, когда значение или строка удаляются или обновляются.
type: docs
weight: 29
url: /ru/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Наследование:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Представляет ограничение действия, применяемое к набору столбцов в отношении первичного/внешнего ключа, когда значение или строка удаляются или обновляются.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---) |  Инициализирует новый экземпляр[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) класс с указанным именем и массивы родительского и дочернего[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) |  Инициализирует новый экземпляр[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) класс с указанным родителем и дочерним элементом[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) |  Инициализирует новый экземпляр[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) класс с указанным именем, родительский и дочерний[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object-) |  Получает значение, указывающее, является ли текущий[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) идентичен указанному объекту. |
| [getClass()](#getClass--) |  |
| [getColumns()](#getColumns--) | Получает дочерние столбцы этого ограничения. |
| [getConstraintName()](#getConstraintName--) |  Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [getDeleteRule()](#getDeleteRule--) | Получает действие, которое происходит с этим ограничением при удалении строки. |
| [getRelatedColumns()](#getRelatedColumns--) | Родительские столбцы этого ограничения. |
| [getRelatedTable()](#getRelatedTable--) | Получает родительскую таблицу этого ограничения. |
| [getTable()](#getTable--) | Получает дочернюю таблицу этого ограничения. |
| [getUpdateRule()](#getUpdateRule--) | Получает действие, которое происходит с этим ограничением при обновлении строки. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String-) |  Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


 Инициализирует новый экземпляр[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) класс с указанным именем и массивы родительского и дочернего[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| constraintName | java.lang.String |  Имя[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint). Если строка нулевая или пустая, при добавлении в коллекцию ограничений будет задано имя по умолчанию. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив родителей[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в ограничении. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив дочерних[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в ограничении. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


 Инициализирует новый экземпляр[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) класс с указанным родителем и дочерним элементом[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Родитель[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в ограничении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Ребенок[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в ограничении. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


 Инициализирует новый экземпляр[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) класс с указанным именем, родительский и дочерний[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| constraintName | java.lang.String | Имя ограничения. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Родитель[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в ограничении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Ребенок[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в ограничении. |

### equals(Object key) {#equals-java.lang.Object-}
```
public boolean equals(Object key)
```


 Получает значение, указывающее, является ли текущий[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) идентичен указанному объекту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | java.lang.Object |  Объект, к которому это[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) сравнивается. Два[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) равны, если они ограничивают одни и те же столбцы. |

**Возвращает:**
boolean - true, если объекты идентичны; в противном случае ложно.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColumns() {#getColumns--}
```
public System.Data.DataColumn[] getColumns()
```


Получает дочерние столбцы этого ограничения.

**Возвращает:**
com.aspose.words.net.System.Data.DataColumn[ ] - Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты, являющиеся дочерними столбцами ограничения.
### getConstraintName() {#getConstraintName--}
```
public String getConstraintName()
```


 Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection).

**Возвращает:**
 java.lang.String — Имя[Constraint](../../com.aspose.words.net.system.data/constraint).
### getDeleteRule() {#getDeleteRule--}
```
public System.Data.Rule getDeleteRule()
```


Получает действие, которое происходит с этим ограничением при удалении строки.

**Возвращает:**
[Rule](../../com.aspose.words.net.system.data/rule) - Один из[Rule](../../com.aspose.words.net.system.data/rule) ценности. По умолчанию Каскад. Возвращаемое значение является одним из[Rule](../../com.aspose.words.net.system.data/rule) константы.
### getRelatedColumns() {#getRelatedColumns--}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Родительские столбцы этого ограничения.

**Возвращает:**
com.aspose.words.net.System.Data.DataColumn[ ] - Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты, являющиеся родительскими столбцами ограничения.
### getRelatedTable() {#getRelatedTable--}
```
public System.Data.DataTable getRelatedTable()
```


Получает родительскую таблицу этого ограничения.

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - Родитель[DataTable](../../com.aspose.words.net.system.data/datatable) этого ограничения.
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


Получает дочернюю таблицу этого ограничения.

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable) это дочерняя таблица в ограничении.
### getUpdateRule() {#getUpdateRule--}
```
public System.Data.Rule getUpdateRule()
```


Получает действие, которое происходит с этим ограничением при обновлении строки.

**Возвращает:**
[Rule](../../com.aspose.words.net.system.data/rule) - Один из[Rule](../../com.aspose.words.net.system.data/rule) ценности. По умолчанию Каскад. Возвращаемое значение является одним из[Rule](../../com.aspose.words.net.system.data/rule) константы.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setConstraintName(String value) {#setConstraintName-java.lang.String-}
```
public void setConstraintName(String value)
```


 Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Имя[Constraint](../../com.aspose.words.net.system.data/constraint). |

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
