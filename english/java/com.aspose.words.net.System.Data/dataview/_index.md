---
title: DataView
linktitle: DataView
second_title: Aspose.Words for Java
description: Represents a databindable customized view of a DataTable for sorting filtering searching editing and navigation in Java.
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

Represents a databindable, customized view of a [DataTable](../../com.aspose.words.net.system.data/datatable/) for sorting, filtering, searching, editing, and navigation.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Initializes a new instance of the [DataView](../../com.aspose.words.net.system.data/dataview/) class with the specified [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Methods

| Method | Description |
| --- | --- |
| [close()](#close) | Closes the [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int recordIndex)](#get-int) | Gets a row of data from a specified table. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of records in the [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [getTable()](#getTable) | Gets the source [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Gets an enumerator for this [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Initializes a new instance of the [DataView](../../com.aspose.words.net.system.data/dataview/) class with the specified [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | A [DataTable](../../com.aspose.words.net.system.data/datatable/) to add to the [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


Closes the [DataView](../../com.aspose.words.net.system.data/dataview/).

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Gets a row of data from a specified table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| recordIndex | int | The index of a record in the [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of records in the [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
int - The number of records in the [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gets the source [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator}
```
public Iterator iterator()
```


Gets an enumerator for this [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
java.util.Iterator - An java.util.Iterator for navigating through the list.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

