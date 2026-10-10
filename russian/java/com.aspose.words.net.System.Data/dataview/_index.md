---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words для Java"
description: "Представляет привязываемый к данным настраиваемый вид DataTable для сортировки, фильтрации, поиска, редактирования и навигации в Java."
type: docs
weight: 28
url: /ru/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Представляет привязываемый к данным, настраиваемый вид [DataTable](../../com.aspose.words.net.system.data/datatable/) для сортировки, фильтрации, поиска, редактирования и навигации.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Создаёт новый экземпляр класса [DataView](../../com.aspose.words.net.system.data/dataview/) с указанным [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Методы

| Метод | Описание |
| --- | --- |
| [close()](#close) | Закрывает [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [get(int recordIndex)](#get-int) | Получает строку данных из указанной таблицы. |
| [getCount()](#getCount) | Получает количество записей в [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [getTable()](#getTable) | Получает исходный [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [iterator()](#iterator) | Получает перечислитель для этого [DataView](../../com.aspose.words.net.system.data/dataview/). |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Создаёт новый экземпляр класса [DataView](../../com.aspose.words.net.system.data/dataview/) с указанным [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Объект [DataTable](../../com.aspose.words.net.system.data/datatable/) для добавления в [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


Закрывает [DataView](../../com.aspose.words.net.system.data/dataview/).

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Получает строку данных из указанной таблицы.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| recordIndex | int | Индекс записи в [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество записей в [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
int - количество записей в [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Получает исходный [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


Получает перечислитель для этого [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
java.util.Iterator - Итератор java.util.Iterator для навигации по списку.
