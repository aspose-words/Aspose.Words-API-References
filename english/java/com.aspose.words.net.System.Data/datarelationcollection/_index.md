---
title: DataRelationCollection
linktitle: DataRelationCollection
second_title: Aspose.Words for Java
description: Represents the collection of DataRelation objects for this DataSet in Java.
type: docs
weight: 19
url: /java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Represents the collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects for this [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Methods

| Method | Description |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Creates a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) with a specified parent and child column, and adds it to the collection. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Adds a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) to the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Adds a relation to the collection. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Adds a relation to the collection. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Creates a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) with the specified name, and parent and child columns, and adds it to the collection. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Creates a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) with the specified name, parent and child columns, with optional constraints according to the value of the  createConstraints  parameter, and adds it to the collection. |
| [clear()](#clear) | Clears the collection of any relations. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Verifies whether a DataRelation with the specific name (case insensitive) exists in the collection. |
| [get(int index)](#get-int) | Gets the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) object at the specified index. |
| [get(String name)](#get-java.lang.String) | Gets the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) object specified by name. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Gets the index of the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) object. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Removes the relation at the specified index from the collection. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Creates a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) with a specified parent and child column, and adds it to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The parent column of the relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The child column of the relation. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Adds a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) to the [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | The DataRelation to add to the collection. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Adds a relation to the collection. Performs no checks on the duplication etc.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | The parent table of the relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | The child table of the relation. |
| parentColumnName | java.lang.String | The parent column's name of the relation. |
| childColumnName | java.lang.String | The child column's name of the relation. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Adds a relation to the collection. Performs no checks on the duplication etc.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | The parent table of the relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | The child table of the relation. |
| parentColumnNames | java.lang.String[] | The array of parent column's name of the relation. |
| childColumnNames | java.lang.String[] | The array of child column's name of the relation. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Creates a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) with the specified name, and parent and child columns, and adds it to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the relation. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The parent column of the relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The child column of the relation. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Creates a [DataRelation](../../com.aspose.words.net.system.data/datarelation/) with the specified name, parent and child columns, with optional constraints according to the value of the  createConstraints  parameter, and adds it to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the relation. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The parent column of the relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The child column of the relation. |
| createConstraints | boolean | true to create constraints; otherwise false. (The default is true). |

### clear() {#clear}
```
public void clear()
```


Clears the collection of any relations.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Verifies whether a DataRelation with the specific name (case insensitive) exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | The name of the relation to find. |

**Returns:**
boolean - true, if a relation with the specified name exists; otherwise false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Gets the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) object at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index to find. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


Gets the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) object specified by name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the relation to find. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - the total number of elements in a collection
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Gets the index of the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | The relation to search for. |

**Returns:**
int - The 0-based index of the relation, or -1 if the relation is not found in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes the relation at the specified index from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The index of the relation to remove. |

