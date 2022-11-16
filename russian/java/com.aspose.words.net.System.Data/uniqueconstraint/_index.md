---
title: UniqueConstraint
second_title: Справочник по API Aspose.Words для Java
description: Представляет ограничение на набор столбцов, в котором все значения должны быть уникальными.
type: docs
weight: 32
url: /ru/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Наследование:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint)
```
public class UniqueConstraint extends System.Data.Constraint
```

Представляет ограничение на набор столбцов, в котором все значения должны быть уникальными.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean-) |  Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с указанным именем, массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения и значение, указывающее, является ли ограничение первичным ключом. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean-) |  Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с массивом[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения и значение, указывающее, является ли ограничение первичным ключом. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---) |  Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с заданным массивом[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты. |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn-) |  Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с указанным[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object-) | Сравнивает это ограничение со вторым, чтобы определить, идентичны ли они оба. |
| [getClass()](#getClass--) |  |
| [getColumns()](#getColumns--) | Получает массив столбцов, на которые влияет это ограничение. |
| [getConstraintName()](#getConstraintName--) |  Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [getTable()](#getTable--) | Получает таблицу, которой принадлежит это ограничение. |
| [hashCode()](#hashCode--) |  |
| [isPrimaryKey()](#isPrimaryKey--) | Получает значение, указывающее, относится ли ограничение к первичному ключу. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String-) |  Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


 Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с указанным именем, массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения и значение, указывающее, является ли ограничение первичным ключом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя ограничения. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения. |
| isPrimaryKey | boolean | Значение true указывает, что ограничение является первичным ключом; в противном случае ложно. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean-}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


 Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с массивом[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения и значение, указывающее, является ли ограничение первичным ключом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения. |
| isPrimaryKey | boolean | Значение true указывает, что ограничение является первичным ключом; в противном случае ложно. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


 Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с заданным массивом[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) |  Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для ограничения. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn-}
```
public UniqueConstraint(System.Data.DataColumn column)
```


 Инициализирует новый экземпляр[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) класс с указанным[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) сдерживать. |

### equals(Object key2) {#equals-java.lang.Object-}
```
public boolean equals(Object key2)
```


Сравнивает это ограничение со вторым, чтобы определить, идентичны ли они оба.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key2 | java.lang.Object |  Объект, к которому это[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint) сравнивается. |

**Возвращает:**
boolean - true, если ограничения равны; в противном случае ложно.
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


Получает массив столбцов, на которые влияет это ограничение.

**Возвращает:**
com.aspose.words.net.System.Data.DataColumn[ ] - Массив[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты.
### getConstraintName() {#getConstraintName--}
```
public String getConstraintName()
```


 Имя ограничения в[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection).

**Возвращает:**
 java.lang.String — Имя[Constraint](../../com.aspose.words.net.system.data/constraint).
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


Получает таблицу, которой принадлежит это ограничение.

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) -[DataTable](../../com.aspose.words.net.system.data/datatable) которому принадлежит ограничение.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isPrimaryKey() {#isPrimaryKey--}
```
public boolean isPrimaryKey()
```


Получает значение, указывающее, относится ли ограничение к первичному ключу.

**Возвращает:**
boolean - true, если ограничение относится к первичному ключу; в противном случае ложно.
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
