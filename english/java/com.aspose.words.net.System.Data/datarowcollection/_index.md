---
title: DataRowCollection
linktitle: DataRowCollection
second_title: Aspose.Words for Java
description: Represents a collection of rows for a DataTable in Java.
type: docs
weight: 21
url: /java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Represents a collection of rows for a [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Methods

| Method | Description |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Adds the specified [DataRow](../../com.aspose.words.net.system.data/datarow/) to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) object. |
| [add(Object[] values)](#add-java.lang.Object...) | Creates a row using specified values and adds it to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [clear()](#clear) | Clears the collection of all rows. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [find(Object[] keys)](#find-java.lang.Object) | Gets the row that contains the specified primary key values. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Gets the row specified by the primary key value. |
| [get(int index)](#get-int) | Gets the row at the specified index. |
| [get(Object[] values)](#get-java.lang.Object) | Gets the row that contains the specified values. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the total number of [DataRow](../../com.aspose.words.net.system.data/datarow/) objects in this collection. |
| [hashCode()](#hashCode) |  |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Inserts a new row into the collection at the specified location. |
| [iterator()](#iterator) | Gets an java.util.Iterator for this collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [removeAt(int index)](#removeAt-int) | Removes the row at the specified index from the collection. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Adds the specified [DataRow](../../com.aspose.words.net.system.data/datarow/) to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | The [DataRow](../../com.aspose.words.net.system.data/datarow/) to add. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Creates a row using specified values and adds it to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| values | java.lang.Object[] | The array of values that are used to create the new row. |

### clear() {#clear}
```
public void clear()
```


Clears the collection of all rows.

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
### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Gets the row that contains the specified primary key values.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| keys | java.lang.Object[] | An array of primary key values to find. The type of the array is Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Gets the row specified by the primary key value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | The primary key value of the DataRow to find. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Gets the row at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the row to return. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Gets the row that contains the specified values. If there is primary key's column(s) present then the index will be used. If there is no index then simple linear scan is used. Be carefully with that because it could take a significant amount of time.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| values | java.lang.Object[] | row's data |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
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


Gets the total number of [DataRow](../../com.aspose.words.net.system.data/datarow/) objects in this collection.

**Returns:**
int - The total number of [DataRow](../../com.aspose.words.net.system.data/datarow/) objects in this collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Inserts a new row into the collection at the specified location.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | The [DataRow](../../com.aspose.words.net.system.data/datarow/) to add. |
| pos | int | The (zero-based) location in the collection where you want to add the DataRow. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Gets an java.util.Iterator for this collection.

**Returns:**
java.util.Iterator - An java.util.Iterator for this collection.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes the row at the specified index from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The index of the row to remove. |

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

