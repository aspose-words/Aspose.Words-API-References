---
title: DataRow
second_title: Справочник по API Aspose.Words для Java
description: Представляет строку данных в файле .
type: docs
weight: 20
url: /ru/java/com.aspose.words.net.system.data/datarow/
---

**Наследование:**
java.lang.Object
```
public class DataRow
```

 Представляет строку данных в[DataTable](../../com.aspose.words.net.system.data/datatable).
## Методы

| Метод | Описание |
| --- | --- |
| [delete()](#delete--) |  Удаляет[DataRow](../../com.aspose.words.net.system.data/datarow). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn-) | Получает данные, хранящиеся в указанном[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [get(int columnIndex)](#get-int-) | Получает данные, хранящиеся в столбце, указанном индексом. |
| [get(String columnName)](#get-java.lang.String-) | Получает данные, хранящиеся в столбце, указанном по имени. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation-) |  Получает дочерние строки этого[DataRow](../../com.aspose.words.net.system.data/datarow) используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getClass()](#getClass--) |  |
| [getItemArray()](#getItemArray--) | Получает все значения для этой строки через массив. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey-) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String-) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation-) |  Получает родительскую строку[DataRow](../../com.aspose.words.net.system.data/datarow) используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation-) |  Получает родительские строки[DataRow](../../com.aspose.words.net.system.data/datarow) используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getRowState()](#getRowState--) |  Получает текущее состояние строки относительно ее отношения к[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection). |
| [getTable()](#getTable--) |  Получает[DataTable](../../com.aspose.words.net.system.data/datatable) для которого эта строка имеет схему. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet-) | Считывает значения из java.sql.ResultSet |
| [remove(int index)](#remove-int-) |  |
| [set(System.Data.DataColumn value, Object column)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object-) |  Устанавливает данные, хранящиеся в указанном[DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [set(int value, Object columnIndex)](#set-int-java.lang.Object-) | Задает данные, хранящиеся в столбце, указанном индексом. |
| [set(String value, Object columnName)](#set-java.lang.String-java.lang.Object-) | Задает данные, хранящиеся в столбце, указанном по имени. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object---) | Устанавливает все значения для этой строки через массив. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object-) |  |
| [setRowState(int state)](#setRowState-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


 Удаляет[DataRow](../../com.aspose.words.net.system.data/datarow).

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
### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn-}
```
public Object get(System.Data.DataColumn column)
```


Получает данные, хранящиеся в указанном[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  А[DataColumn](../../com.aspose.words.net.system.data/datacolumn) который содержит данные. |

**Возвращает:**
java.lang.Object — объект java.lang.Object, содержащий данные.
### get(int columnIndex) {#get-int-}
```
public Object get(int columnIndex)
```


Получает данные, хранящиеся в столбце, указанном индексом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnIndex | int | Отсчитываемый от нуля индекс столбца. |

**Возвращает:**
java.lang.Object — объект java.lang.Object, содержащий данные.
### get(String columnName) {#get-java.lang.String-}
```
public Object get(String columnName)
```


Получает данные, хранящиеся в столбце, указанном по имени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца. |

**Возвращает:**
java.lang.Object — объект java.lang.Object, содержащий данные.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


 Получает дочерние строки этого[DataRow](../../com.aspose.words.net.system.data/datarow) используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | [DataRelation](../../com.aspose.words.net.system.data/datarelation) использовать. |

**Возвращает:**
com.aspose.words.net.System.Data.DataRow[ ] - Массив[DataRow](../../com.aspose.words.net.system.data/datarow) объекты или массив нулевой длины.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getItemArray() {#getItemArray--}
```
public Object[] getItemArray()
```


Получает все значения для этой строки через массив.

**Возвращает:**
java.lang.Объект[— Массив типа java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey-}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey) |  |

**Возвращает:**
java.lang.Объект[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String-}
```
public Object getOriginalValue(String columnName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Возвращает:**
java.lang.Объект
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


 Получает родительскую строку[DataRow](../../com.aspose.words.net.system.data/datarow) используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | [DataRelation](../../com.aspose.words.net.system.data/datarelation) использовать. |

**Возвращает:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - Родитель[DataRow](../../com.aspose.words.net.system.data/datarow) текущей строки.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


 Получает родительские строки[DataRow](../../com.aspose.words.net.system.data/datarow) используя указанный[DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | [DataRelation](../../com.aspose.words.net.system.data/datarelation) использовать. |

**Возвращает:**
com.aspose.words.net.System.Data.DataRow[ ] - Массив[DataRow](../../com.aspose.words.net.system.data/datarow) объекты или массив нулевой длины.
### getRowState() {#getRowState--}
```
public int getRowState()
```


 Получает текущее состояние строки относительно ее отношения к[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).

**Возвращает:**
 инт - один из[DataRowState](../../com.aspose.words.net.system.data/datarowstate) ценности. Возвращаемое значение представляет собой побитовую комбинацию[DataRowState](../../com.aspose.words.net.system.data/datarowstate) константы.
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


 Получает[DataTable](../../com.aspose.words.net.system.data/datatable) для которого эта строка имеет схему.

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) -[DataTable](../../com.aspose.words.net.system.data/datatable) которому принадлежит этот ряд.
### hashCode() {#hashCode--}
```
public native int hashCode()
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




### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet-}
```
public boolean readFrom(ResultSet resultSet)
```


Считывает значения из java.sql.ResultSet

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | хранилище для чтения |

**Возвращает:**
boolean - истина, если не было ошибок чтения
### remove(int index) {#remove-int-}
```
public void remove(int index)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |

### set(System.Data.DataColumn value, Object column) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object-}
```
public void set(System.Data.DataColumn value, Object column)
```


 Устанавливает данные, хранящиеся в указанном[DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Объект java.lang.Object, содержащий данные. |
| column | java.lang.Object |  А[DataColumn](../../com.aspose.words.net.system.data/datacolumn) который содержит данные. |

### set(int value, Object columnIndex) {#set-int-java.lang.Object-}
```
public void set(int value, Object columnIndex)
```


Задает данные, хранящиеся в столбце, указанном индексом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Объект java.lang.Object, содержащий данные. |
| columnIndex | java.lang.Object | Отсчитываемый от нуля индекс столбца. |

### set(String value, Object columnName) {#set-java.lang.String-java.lang.Object-}
```
public void set(String value, Object columnName)
```


Задает данные, хранящиеся в столбце, указанном по имени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Объект java.lang.Object, содержащий данные. |
| columnName | java.lang.Object | Имя столбца. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object---}
```
public void setItemArray(Object[] value)
```


Устанавливает все значения для этой строки через массив.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object[] | Массив типа java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object-}
```
public void setOriginalValue(String columnName, Object data)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String |  |
| data | java.lang.Object |  |

### setRowState(int state) {#setRowState-int-}
```
public void setRowState(int state)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| state | int |  |

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
