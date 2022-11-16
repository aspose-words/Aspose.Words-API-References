---
title: DataTableCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию таблиц для .
type: docs
weight: 26
url: /ru/java/com.aspose.words.net.system.data/datatablecollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

 Представляет набор таблиц для[DataSet](../../com.aspose.words.net.system.data/dataset).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable-) | Добавляет указанный DataTable в коллекцию. |
| [add(String name)](#add-java.lang.String-) |  Создает[DataTable](../../com.aspose.words.net.system.data/datatable) объект с использованием указанного имени и добавляет его в коллекцию. |
| [contains(String name)](#contains-java.lang.String-) |  Получает значение, указывающее, является ли[DataTable](../../com.aspose.words.net.system.data/datatable) объект с указанным именем существует в коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Получает[DataTable](../../com.aspose.words.net.system.data/datatable) объект по указанному индексу. |
| [get(String name)](#get-java.lang.String-) |  Получает[DataTable](../../com.aspose.words.net.system.data/datatable) объект с указанным именем. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String-) |  Получает[DataTable](../../com.aspose.words.net.system.data/datatable) объект с указанным именем в указанном пространстве имен. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable-}
```
public void add(System.Data.DataTable table)
```


Добавляет указанный DataTable в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | Добавляемый объект DataTable. |

### add(String name) {#add-java.lang.String-}
```
public System.Data.DataTable add(String name)
```


 Создает[DataTable](../../com.aspose.words.net.system.data/datatable) объект с использованием указанного имени и добавляет его в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  Имя, которое нужно дать созданному[DataTable](../../com.aspose.words.net.system.data/datatable). |

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - Вновь созданный[DataTable](../../com.aspose.words.net.system.data/datatable).
### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


 Получает значение, указывающее, является ли[DataTable](../../com.aspose.words.net.system.data/datatable) объект с указанным именем существует в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  Имя[DataTable](../../com.aspose.words.net.system.data/datatable) найти. |

**Возвращает:**
boolean - true, если указанная таблица существует; иначе ложно.
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
public System.Data.DataTable get(int index)
```


 Получает[DataTable](../../com.aspose.words.net.system.data/datatable) объект по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  Отсчитываемый от нуля индекс[DataTable](../../com.aspose.words.net.system.data/datatable) найти. |

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable).
### get(String name) {#get-java.lang.String-}
```
public System.Data.DataTable get(String name)
```


 Получает[DataTable](../../com.aspose.words.net.system.data/datatable) объект с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя DataTable для поиска. |

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable) с указанным именем; в противном случае null, если[DataTable](../../com.aspose.words.net.system.data/datatable) не существует.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String-}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


 Получает[DataTable](../../com.aspose.words.net.system.data/datatable) объект с указанным именем в указанном пространстве имен.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя DataTable для поиска. |
| tableNamespace | java.lang.String |  Имя[DataTable](../../com.aspose.words.net.system.data/datatable) пространство имен для поиска. |

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable) с указанным именем; в противном случае null, если[DataTable](../../com.aspose.words.net.system.data/datatable) не существует.
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
int - общее количество элементов в этой коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
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
