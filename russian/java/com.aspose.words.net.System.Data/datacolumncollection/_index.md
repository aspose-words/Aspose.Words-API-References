---
title: DataColumnCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию объектов для .
type: docs
weight: 15
url: /ru/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

 Представляет собой совокупность[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объекты для[DataTable](../../com.aspose.words.net.system.data/datatable).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn-) |  Создает и добавляет указанный[DataColumn](../../com.aspose.words.net.system.data/datacolumn) возражать против[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [add(String columnName)](#add-java.lang.String-) |  Создает и добавляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объект с указанным именем для[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class-) |  Создает и добавляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объект с указанным именем и типом для[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean-) |  Создает и добавляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) с указанным именем, типом и конкретными значениями в коллекцию столбцов. |
| [clear()](#clear--) | Очищает коллекцию любых столбцов. |
| [contains(String name)](#contains-java.lang.String-) | Проверяет, содержит ли коллекция столбец с указанным именем. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Получает[DataColumn](../../com.aspose.words.net.system.data/datacolumn) из коллекции по указанному индексу. |
| [get(String name)](#get-java.lang.String-) |  Получает[DataColumn](../../com.aspose.words.net.system.data/datacolumn) из коллекции с указанным именем. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn-) | Получает индекс столбца, указанного по имени. |
| [indexOf(String columnName)](#indexOf-java.lang.String-) | Получает индекс столбца с определенным именем (имя не чувствительно к регистру). |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn-) |  Удаляет указанный[DataColumn](../../com.aspose.words.net.system.data/datacolumn) предмет из коллекции. |
| [remove(String name)](#remove-java.lang.String-) |  Удаляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объект с указанным именем из коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn-}
```
public void add(System.Data.DataColumn column)
```


 Создает и добавляет указанный[DataColumn](../../com.aspose.words.net.system.data/datacolumn) возражать против[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) добавить. |

### add(String columnName) {#add-java.lang.String-}
```
public void add(String columnName)
```


 Создает и добавляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объект с указанным именем для[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class-}
```
public System.Data.DataColumn add(String columnName, Class type)
```


 Создает и добавляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объект с указанным именем и типом для[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) для использования при создании столбца. |
| type | java.lang.Class | [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn\#getDataType--) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn\#setDataType-java.lang.Class-) новой колонки. |

**Возвращает:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) - Вновь созданный[DataColumn](../../com.aspose.words.net.system.data/datacolumn).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean-}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


 Создает и добавляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) с указанным именем, типом и конкретными значениями в коллекцию столбцов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | имя |
| type | java.lang.Class | тип данных |
| columnMapping | int | тип сопоставления столбцов |
| allowAutoIncrement | boolean | разрешено ли автоматическое увеличение |
| allowDBNull | boolean | допустимо ли значение DBNull |

**Возвращает:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) - создал[DataColumn](../../com.aspose.words.net.system.data/datacolumn) пример.
### clear() {#clear--}
```
public void clear()
```


Очищает коллекцию любых столбцов.

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Проверяет, содержит ли коллекция столбец с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) столбца для поиска. |

**Возвращает:**
boolean - true, если столбец с таким именем существует; в противном случае ложно.
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
### get(int index) {#get-int-}
```
public System.Data.DataColumn get(int index)
```


 Получает[DataColumn](../../com.aspose.words.net.system.data/datacolumn) из коллекции по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс возвращаемого столбца. |

**Возвращает:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) -[DataColumn](../../com.aspose.words.net.system.data/datacolumn) по указанному индексу.
### get(String name) {#get-java.lang.String-}
```
public System.Data.DataColumn get(String name)
```


 Получает[DataColumn](../../com.aspose.words.net.system.data/datacolumn) из коллекции с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) столбца для возврата. |

**Возвращает:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn) -[DataColumn](../../com.aspose.words.net.system.data/datacolumn) в сборе с указанным[DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn\#getColumnName--) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn\#setColumnName-java.lang.String-) ; в противном случае нулевое значение, если[DataColumn](../../com.aspose.words.net.system.data/datacolumn) не существует.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```




**Возвращает:**
int - общее количество элементов в коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn-}
```
public int indexOf(System.Data.DataColumn column)
```


Получает индекс столбца, указанного по имени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Имя возвращаемого столбца. |

**Возвращает:**
int - Индекс столбца, заданный столбцом, если он найден; иначе -1.
### indexOf(String columnName) {#indexOf-java.lang.String-}
```
public int indexOf(String columnName)
```


Получает индекс столбца с определенным именем (имя не чувствительно к регистру).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| columnName | java.lang.String | Имя столбца, который необходимо найти. |

**Возвращает:**
int — отсчитываемый от нуля индекс столбца с указанным именем или -1, если столбец не существует в коллекции.
### iterator() {#iterator--}
```
public Iterator iterator()
```




**Возвращает:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn-}
```
public void remove(System.Data.DataColumn column)
```


 Удаляет указанный[DataColumn](../../com.aspose.words.net.system.data/datacolumn) предмет из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) удалять. |

### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


 Удаляет[DataColumn](../../com.aspose.words.net.system.data/datacolumn) объект с указанным именем из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя столбца, который необходимо удалить. |

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
