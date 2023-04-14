---
title: DataTableCollection
linktitle: DataTableCollection
second_title: Aspose.Words for Java API Reference
description: Represents the collection of tables for the DataSet in Java.
type: docs
weight: 26
url: /java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

Represents the collection of tables for the [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Methods

| Method | Description |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Adds the specified DataTable to the collection. |
| [add(String name)](#add-java.lang.String) | Creates a [DataTable](../../com.aspose.words.net.system.data/datatable/) object by using the specified name and adds it to the collection. |
| [contains(String name)](#contains-java.lang.String) | Gets a value that indicates whether a [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name exists in the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object at the specified index. |
| [get(String name)](#get-java.lang.String) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name in the specified namespace. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) |  |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Adds the specified DataTable to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | The DataTable object to add. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Creates a [DataTable](../../com.aspose.words.net.system.data/datatable/) object by using the specified name and adds it to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name to give the created [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Gets a value that indicates whether a [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the [DataTable](../../com.aspose.words.net.system.data/datatable/) to find. |

**Returns:**
boolean - true if the specified table exists; otherwise false.
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
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the [DataTable](../../com.aspose.words.net.system.data/datatable/) to find. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the DataTable to find. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name in the specified namespace.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the DataTable to find. |
| tableNamespace | java.lang.String | The name of the [DataTable](../../com.aspose.words.net.system.data/datatable/) namespace to look in. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
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




**Returns:**
int - total number of items in this collection.
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




**Returns:**
java.util.Iterator
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

