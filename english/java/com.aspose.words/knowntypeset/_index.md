---
title: KnownTypeSet
linktitle: KnownTypeSet
second_title: Aspose.Words for Java API Reference
description: Represents an unordered set i.e in Java.
type: docs
weight: 360
url: /java/com.aspose.words/knowntypeset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

Represents an unordered set (i.e. a collection of unique items) containing java.lang.Class objects which fully or partially qualified names can be used within report templates to invoke the corresponding types' static members, perform type casts, etc.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Methods

| Method | Description |
| --- | --- |
| [add(Class type)](#add-java.lang.Class) | Adds the specified java.lang.Class object to the set. |
| [clear()](#clear) | Removes all items from the set. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the count of items in the set. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns An java.util.Iterator object to iterate over items of the set. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(Class type)](#remove-java.lang.Class) | Removes the specified java.lang.Class object from the set. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(Class type) {#add-java.lang.Class}
```
public void add(Class type)
```


Adds the specified java.lang.Class object to the set. Throws java.lang.IllegalArgumentException in the following cases:

\-  type  is  null .

\-  type  represents a void type.

\-  type  represents an invisible type, i.e. a non-public type or a public nested type which has a non-public outer type.

\-  type  represents an array type.

\-  type  has been added to the set already.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | java.lang.Class | A java.lang.Class object to add. |

### clear() {#clear}
```
public void clear()
```


Removes all items from the set.

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


Gets the count of items in the set.

**Returns:**
int - The count of items in the set.
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


Returns An java.util.Iterator object to iterate over items of the set.

**Returns:**
java.util.Iterator - An java.util.Iterator object to iterate over items of the set.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove(Class type) {#remove-java.lang.Class}
```
public void remove(Class type)
```


Removes the specified java.lang.Class object from the set. Throws java.lang.IllegalArgumentException if  type  is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | java.lang.Class | A java.lang.Class object to remove. |

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

