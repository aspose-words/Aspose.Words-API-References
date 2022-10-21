---
title: DataView
second_title: Aspose.Words for Java API Reference
description: Represents a databindable customized view of a  for sorting filtering searching editing and navigation.
type: docs
weight: 28
url: /java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Represents a databindable, customized view of a [DataTable](../../com.aspose.words.net.system.data/datatable) for sorting, filtering, searching, editing, and navigation.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable-) | Initializes a new instance of the [DataView](../../com.aspose.words.net.system.data/dataview) class with the specified [DataTable](../../com.aspose.words.net.system.data/datatable). |
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of records in the [DataView](../../com.aspose.words.net.system.data/dataview). |
| [getTable()](#getTable--) | Gets the source [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [get(int recordIndex)](#get-int-) | Gets a row of data from a specified table. |
| [close()](#close--) | Closes the [DataView](../../com.aspose.words.net.system.data/dataview). |
| [iterator()](#iterator--) | Gets an enumerator for this [DataView](../../com.aspose.words.net.system.data/dataview). |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable-}
```
public DataView(System.Data.DataTable table)
```


Initializes a new instance of the [DataView](../../com.aspose.words.net.system.data/dataview) class with the specified [DataTable](../../com.aspose.words.net.system.data/datatable).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | A [DataTable](../../com.aspose.words.net.system.data/datatable) to add to the [DataView](../../com.aspose.words.net.system.data/dataview). |

### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of records in the [DataView](../../com.aspose.words.net.system.data/dataview).

**Returns:**
int - The number of records in the [DataView](../../com.aspose.words.net.system.data/dataview).
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


Gets the source [DataTable](../../com.aspose.words.net.system.data/datatable).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - A [DataTable](../../com.aspose.words.net.system.data/datatable) that provides the data for this view.
### get(int recordIndex) {#get-int-}
```
public System.Data.DataRowView get(int recordIndex)
```


Gets a row of data from a specified table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| recordIndex | int | The index of a record in the [DataTable](../../com.aspose.words.net.system.data/datatable). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview) of the row that you want.
### close() {#close--}
```
public void close()
```


Closes the [DataView](../../com.aspose.words.net.system.data/dataview).

### iterator() {#iterator--}
```
public Iterator iterator()
```


Gets an enumerator for this [DataView](../../com.aspose.words.net.system.data/dataview).

**Returns:**
java.util.Iterator - An java.util.Iterator for navigating through the list.
