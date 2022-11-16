---
title: DataView
second_title: Справочник по API Aspose.Words для Java
description: Представляет настраиваемое представление с привязкой к данным для сортировки, фильтрации, поиска, редактирования и навигации.
type: docs
weight: 28
url: /ru/java/com.aspose.words.net.system.data/dataview/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class DataView implements Iterable
```

 Представляет привязываемое к данным настраиваемое представление[DataTable](../../com.aspose.words.net.system.data/datatable) для сортировки, фильтрации, поиска, редактирования и навигации.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable-) |  Инициализирует новый экземпляр[DataView](../../com.aspose.words.net.system.data/dataview) класс с указанным[DataTable](../../com.aspose.words.net.system.data/datatable). |
## Методы

| Метод | Описание |
| --- | --- |
| [close()](#close--) |  Закрывает[DataView](../../com.aspose.words.net.system.data/dataview). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int recordIndex)](#get-int-) | Получает строку данных из указанной таблицы. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  Получает количество записей в[DataView](../../com.aspose.words.net.system.data/dataview). |
| [getTable()](#getTable--) |  Получает источник[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) |  Получает перечислитель для этого[DataView](../../com.aspose.words.net.system.data/dataview). |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable-}
```
public DataView(System.Data.DataTable table)
```


 Инициализирует новый экземпляр[DataView](../../com.aspose.words.net.system.data/dataview) класс с указанным[DataTable](../../com.aspose.words.net.system.data/datatable).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) |  А[DataTable](../../com.aspose.words.net.system.data/datatable) добавить к[DataView](../../com.aspose.words.net.system.data/dataview). |

### close() {#close--}
```
public void close()
```


 Закрывает[DataView](../../com.aspose.words.net.system.data/dataview).

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
### get(int recordIndex) {#get-int-}
```
public System.Data.DataRowView get(int recordIndex)
```


Получает строку данных из указанной таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| recordIndex | int |  Индекс записи в[DataTable](../../com.aspose.words.net.system.data/datatable). |

**Возвращает:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview) - А[DataRowView](../../com.aspose.words.net.system.data/datarowview) строки, которую вы хотите.
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


 Получает количество записей в[DataView](../../com.aspose.words.net.system.data/dataview).

**Возвращает:**
 int - количество записей в[DataView](../../com.aspose.words.net.system.data/dataview).
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


 Получает источник[DataTable](../../com.aspose.words.net.system.data/datatable).

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable) который предоставляет данные для этого представления.
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


 Получает перечислитель для этого[DataView](../../com.aspose.words.net.system.data/dataview).

**Возвращает:**
java.util.Iterator — java.util.Iterator для навигации по списку.
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
