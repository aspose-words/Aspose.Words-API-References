---
title: DataRelationCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию объектов для этого .
type: docs
weight: 19
url: /ru/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

 Представляет собой коллекцию[DataRelation](../../com.aspose.words.net.system.data/datarelation) объекты для этого[DataSet](../../com.aspose.words.net.system.data/dataset).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) |  Создает[DataRelation](../../com.aspose.words.net.system.data/datarelation) с указанным родительским и дочерним столбцом и добавляет его в коллекцию. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation-) |  Добавляет[DataRelation](../../com.aspose.words.net.system.data/datarelation) к[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String-) | Добавляет отношение к коллекции. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---) | Добавляет отношение к коллекции. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-) |  Создает[DataRelation](../../com.aspose.words.net.system.data/datarelation) с указанным именем, родительским и дочерним столбцами и добавляет его в коллекцию. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-) |  Создает[DataRelation](../../com.aspose.words.net.system.data/datarelation) с указанным именем, родительским и дочерним столбцами, с необязательными ограничениями в соответствии со значением параметра createConstraints, и добавляет его в коллекцию. |
| [clear()](#clear--) | Очищает коллекцию любых отношений. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation-) | Проверяет, существует ли в коллекции объект DataRelation с определенным именем (без учета регистра). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Получает[DataRelation](../../com.aspose.words.net.system.data/datarelation) объект по указанному индексу. |
| [get(String name)](#get-java.lang.String-) |  Получает[DataRelation](../../com.aspose.words.net.system.data/datarelation) объект, указанный по имени. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation-) |  Получает индекс указанного[DataRelation](../../com.aspose.words.net.system.data/datarelation) объект. |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | Удаляет отношение по указанному индексу из коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


 Создает[DataRelation](../../com.aspose.words.net.system.data/datarelation) с указанным родительским и дочерним столбцом и добавляет его в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Родительский столбец отношения. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Дочерний столбец отношения. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation-}
```
public void add(System.Data.DataRelation relation)
```


 Добавляет[DataRelation](../../com.aspose.words.net.system.data/datarelation) к[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | DataRelation для добавления в коллекцию. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String-}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Добавляет отношение к коллекции. Не выполняет проверки на дублирование и т.д.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | Родительская таблица отношения. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | Дочерняя таблица отношения. |
| parentColumnName | java.lang.String | Имя родительского столбца отношения. |
| childColumnName | java.lang.String | Имя дочернего столбца отношения. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String---}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Добавляет отношение к коллекции. Не выполняет проверки на дублирование и т.д.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | Родительская таблица отношения. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | Дочерняя таблица отношения. |
| parentColumnNames | java.lang.String[] | Массив имени родительского столбца отношения. |
| childColumnNames | java.lang.String[] | Массив имен дочерних столбцов отношения. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


 Создает[DataRelation](../../com.aspose.words.net.system.data/datarelation) с указанным именем, родительским и дочерним столбцами и добавляет его в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя отношения. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Родительский столбец отношения. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Дочерний столбец отношения. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean-}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


 Создает[DataRelation](../../com.aspose.words.net.system.data/datarelation) с указанным именем, родительским и дочерним столбцами, с необязательными ограничениями в соответствии со значением параметра createConstraints, и добавляет его в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя отношения. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Родительский столбец отношения. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | Дочерний столбец отношения. |
| createConstraints | boolean | true для создания ограничений; иначе ложно. (По умолчанию верно). |

### clear() {#clear--}
```
public void clear()
```


Очищает коллекцию любых отношений.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation-}
```
public boolean contains(System.Data.DataRelation relation)
```


Проверяет, существует ли в коллекции объект DataRelation с определенным именем (без учета регистра).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | Имя отношения, которое необходимо найти. |

**Возвращает:**
boolean - true, если отношение с указанным именем существует; иначе ложно.
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
public System.Data.DataRelation get(int index)
```


 Получает[DataRelation](../../com.aspose.words.net.system.data/datarelation) объект по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс для поиска. |

**Возвращает:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation) -[DataRelation](../../com.aspose.words.net.system.data/datarelation) или нулевое значение, если указано[DataRelation](../../com.aspose.words.net.system.data/datarelation) не существует.
### get(String name) {#get-java.lang.String-}
```
public System.Data.DataRelation get(String name)
```


 Получает[DataRelation](../../com.aspose.words.net.system.data/datarelation) объект, указанный по имени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя отношения, которое необходимо найти. |

**Возвращает:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation) - Названный[DataRelation](../../com.aspose.words.net.system.data/datarelation) или нулевое значение, если указано[DataRelation](../../com.aspose.words.net.system.data/datarelation) не существует.
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
int - общее количество элементов в коллекции
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation-}
```
public int indexOf(System.Data.DataRelation relation)
```


 Получает индекс указанного[DataRelation](../../com.aspose.words.net.system.data/datarelation) объект.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | Отношение к поиску. |

**Возвращает:**
int — индекс отношения, начинающийся с 0, или -1, если отношение не найдено в коллекции.
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




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет отношение по указанному индексу из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс отношения для удаления. |

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
