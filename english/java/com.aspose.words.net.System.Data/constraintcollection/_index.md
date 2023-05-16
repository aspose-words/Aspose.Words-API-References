---
title: ConstraintCollection
linktitle: ConstraintCollection
second_title: Aspose.Words for Java
description: Represents a collection of constraints for a DataTable in Java.
type: docs
weight: 11
url: /java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Represents a collection of constraints for a [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Methods

| Method | Description |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Adds the specified [Constraint](../../com.aspose.words.net.system.data/constraint/) object to the collection. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | Indicates whether the Constraint object specified by name exists in the collection. |
| [get(int index)](#get-int) | Gets the [Constraint](../../com.aspose.words.net.system.data/constraint/) from the collection at the specified index. |
| [get(String name)](#get-java.lang.String) | Gets the [Constraint](../../com.aspose.words.net.system.data/constraint/) from the collection with the specified name. |
| [getCount()](#getCount) | Gets the total number of elements in a collection. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Removes the specified [Constraint](../../com.aspose.words.net.system.data/constraint/) from the collection. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Adds the specified [Constraint](../../com.aspose.words.net.system.data/constraint/) object to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | The Constraint to add. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


Indicates whether the Constraint object specified by name exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | The Constraint to remove. |

**Returns:**
boolean - true if the collection contains the specified constraint; otherwise, false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Gets the [Constraint](../../com.aspose.words.net.system.data/constraint/) from the collection at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The index of the constraint to return. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Gets the [Constraint](../../com.aspose.words.net.system.data/constraint/) from the collection with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) of the constraint to return. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Gets the total number of elements in a collection.

**Returns:**
int - The total number of elements in a collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint}
```
public void remove(System.Data.Constraint constraint)
```


Removes the specified [Constraint](../../com.aspose.words.net.system.data/constraint/) from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | The [Constraint](../../com.aspose.words.net.system.data/constraint/) to remove. |

