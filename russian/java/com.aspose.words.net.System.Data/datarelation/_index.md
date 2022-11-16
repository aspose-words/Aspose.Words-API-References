---
title: DataRelation
second_title: Справочник по API Aspose.Words для Java
description: Представляет родительско-дочернюю связь между двумя объектами.
type: docs
weight: 18
url: /ru/java/com.aspose.words.net.system.data/datarelation/
---

**Наследование:**
java.lang.Object
```
public class DataRelation
```

 Представляет родительско-дочерние отношения между двумя[DataTable](../../com.aspose.words.net.system.data/datatable) объекты.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---) |  Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, используя указанное имя, родительские и дочерние таблицы, сопоставленные массивы родительских и дочерних столбцов. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean-) |  Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, использующий указанное имя, сопоставленные массивы родительского и дочернего[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты и значение, указывающее, следует ли создавать ограничения. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-) |  Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, использующий указанное имя, родительский и дочерний[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты и значение, указывающее, создавать ли ограничения. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) |  Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation) имя, родитель и ребенок[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getChildColumnNames()](#getChildColumnNames--) |  |
| [getChildColumns()](#getChildColumns--) |  Получает ребенка[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты этого отношения. |
| [getChildKey()](#getChildKey--) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint--) |  Получает[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) для отношения. |
| [getChildTable()](#getChildTable--) | Получает дочернюю таблицу этого отношения. |
| [getChildTableName()](#getChildTableName--) |  |
| [getClass()](#getClass--) |  |
| [getDataSet()](#getDataSet--) |  Получает[DataSet](../../com.aspose.words.net.system.data/dataset) к которому[DataRelation](../../com.aspose.words.net.system.data/datarelation) принадлежит. |
| [getParentColumnNames()](#getParentColumnNames--) |  |
| [getParentColumns()](#getParentColumns--) |  Получает массив из[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты, которые являются родительскими столбцами этого[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentKey()](#getParentKey--) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint--) |  Получает[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) что гарантирует, что значения в родительском столбце[DataRelation](../../com.aspose.words.net.system.data/datarelation) уникальны. |
| [getParentTable()](#getParentTable--) |  Получает родителя[DataTable](../../com.aspose.words.net.system.data/datatable) этого[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentTableName()](#getParentTableName--) |  |
| [getRelationName()](#getRelationName--) |  Получает имя, используемое для получения[DataRelation](../../com.aspose.words.net.system.data/datarelation) от[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint-) |  |
| [setNested(boolean value)](#setNested-boolean-) |  Устанавливает значение, указывающее,[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты вложены. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


 Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, используя указанное имя, родительские и дочерние таблицы, сопоставленные массивы родительских и дочерних столбцов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String | Имя отношения данных. Если значение null или пустая строка (""), имя по умолчанию будет присвоено при добавлении созданного объекта в DataRelationCollection. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | Родительская таблица в отношении. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | Дочерняя таблица в отношении. |
| parentColumnNames | java.lang.String[] | Имя родительского столбца данных в отношении. |
| childColumnNames | java.lang.String[] | Дочерний столбец данных в отношении. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


 Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, использующий указанное имя, сопоставленные массивы родительского и дочернего[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты и значение, указывающее, следует ли создавать ограничения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String |  Имя отношения. Если значение null или пустая строка (""), имя по умолчанию будет присвоено при добавлении созданного объекта в[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив родителей[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив дочерних[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
| createConstraints | boolean | Значение, указывающее, следует ли создавать ограничения. true, если ограничения созданы. В противном случае ложно. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


 Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, использующий указанное имя, родительский и дочерний[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты и значение, указывающее, создавать ли ограничения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String |  Имя отношения. Если значение null или пустая строка (""), имя по умолчанию будет присвоено при добавлении созданного объекта в[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Родитель[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в отношении. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Ребенок[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в отношении. |
| createConstraints | boolean | Значение, указывающее, созданы ли ограничения. true, если ограничения созданы. В противном случае ложно. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


 Инициализирует новый экземпляр[DataRelation](../../com.aspose.words.net.system.data/datarelation) класс, используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation) имя, родитель и ребенок[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relationName | java.lang.String |  Имя[DataRelation](../../com.aspose.words.net.system.data/datarelation) . Если значение null или пустая строка (""), имя по умолчанию будет присвоено при добавлении созданного объекта в[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Родитель[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в отношениях. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  Ребенок[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в отношениях. |

### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### getChildColumnNames() {#getChildColumnNames--}
```
public String[] getChildColumnNames()
```




**Возвращает:**
java.lang.String[] - имена дочерних DataColumn этого отношения.
### getChildColumns() {#getChildColumns--}
```
public System.Data.DataColumn[] getChildColumns()
```


 Получает ребенка[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты этого отношения.

**Возвращает:**
com.aspose.words.net.System.Data.DataColumn[ ] - Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.
### getChildKey() {#getChildKey--}
```
public System.Data.DataKey getChildKey()
```




**Возвращает:**
[DataKey](../../com.aspose.words.net.system.data/datakey)
### getChildKeyConstraint() {#getChildKeyConstraint--}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


 Получает[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) для отношения.

**Возвращает:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) - А[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint).
### getChildTable() {#getChildTable--}
```
public System.Data.DataTable getChildTable()
```


Получает дочернюю таблицу этого отношения.

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable) это дочерняя таблица отношения.
### getChildTableName() {#getChildTableName--}
```
public String getChildTableName()
```




**Возвращает:**
java.lang.String — имя дочерней DataTable этого DataRelation.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDataSet() {#getDataSet--}
```
public System.Data.DataSet getDataSet()
```


 Получает[DataSet](../../com.aspose.words.net.system.data/dataset) к которому[DataRelation](../../com.aspose.words.net.system.data/datarelation) принадлежит.

**Возвращает:**
[DataSet](../../com.aspose.words.net.system.data/dataset) - А[DataSet](../../com.aspose.words.net.system.data/dataset) к которому[DataRelation](../../com.aspose.words.net.system.data/datarelation) принадлежит.
### getParentColumnNames() {#getParentColumnNames--}
```
public String[] getParentColumnNames()
```




**Возвращает:**
java.lang.String[] - имена родительских DataColumn этого отношения.
### getParentColumns() {#getParentColumns--}
```
public System.Data.DataColumn[] getParentColumns()
```


 Получает массив из[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты, которые являются родительскими столбцами этого[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Возвращает:**
com.aspose.words.net.System.Data.DataColumn[ ] - Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты, которые являются родительскими столбцами этого[DataRelation](../../com.aspose.words.net.system.data/datarelation).
### getParentKey() {#getParentKey--}
```
public System.Data.DataKey getParentKey()
```




**Возвращает:**
[DataKey](../../com.aspose.words.net.system.data/datakey)
### getParentKeyConstraint() {#getParentKeyConstraint--}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


 Получает[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) что гарантирует, что значения в родительском столбце[DataRelation](../../com.aspose.words.net.system.data/datarelation) уникальны.

**Возвращает:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) - А[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) это гарантирует, что значения в родительском столбце уникальны.
### getParentTable() {#getParentTable--}
```
public System.Data.DataTable getParentTable()
```


 Получает родителя[DataTable](../../com.aspose.words.net.system.data/datatable) этого[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable) это родительская таблица этого отношения.
### getParentTableName() {#getParentTableName--}
```
public String getParentTableName()
```




**Возвращает:**
java.lang.String — имя родительской DataTable этого DataRelation.
### getRelationName() {#getRelationName--}
```
public String getRelationName()
```


 Получает имя, используемое для получения[DataRelation](../../com.aspose.words.net.system.data/datarelation) от[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection).

**Возвращает:**
 java.lang.String — Имя[DataRelation](../../com.aspose.words.net.system.data/datarelation).
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




### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint-}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) |  |

### setNested(boolean value) {#setNested-boolean-}
```
public void setNested(boolean value)
```


 Устанавливает значение, указывающее,[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты вложены.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  правда, если[DataRelation](../../com.aspose.words.net.system.data/datarelation)объекты вложены друг в друга; в противном случае ложно. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint-}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) |  |

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
