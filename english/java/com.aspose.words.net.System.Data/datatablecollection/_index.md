---
title: DataTableCollection
linktitle: DataTableCollection
second_title: Aspose.Words for Java
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
| [get(int index)](#get-int) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object at the specified index. |
| [get(String name)](#get-java.lang.String) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name in the specified namespace. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Removes the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name from the collection. |
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
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - total number of items in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


Removes the [DataTable](../../com.aspose.words.net.system.data/datatable/) object with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the [DataTable](../../com.aspose.words.net.system.data/datatable/) object to remove. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
