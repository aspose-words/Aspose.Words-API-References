---
title: MappedDataFieldCollection
linktitle: MappedDataFieldCollection
second_title: Aspose.Words for Java API Reference
description: Allows to automatically map between names of fields in your data source and names of mail merge fields in the document in Java.
type: docs
weight: 390
url: /java/com.aspose.words/mappeddatafieldcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class MappedDataFieldCollection implements Iterable
```

Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.

To learn more, visit the [ Mail Merge and Reporting ][Mail Merge and Reporting] documentation article.

This is implemented as a collection of string keys into string values. The keys are the names of mail merge fields in the document and the values are the names of fields in your data source.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methods

| Method | Description |
| --- | --- |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String) | Adds a new field mapping. |
| [clear()](#clear) | Removes all elements from the collection. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String) | Determines whether a mapping from the specified field in the document exists in the collection. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String) | Determines whether a mapping from the specified field in the data source exists in the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(String documentFieldName)](#get-java.lang.String) | Gets the name of the field in the data source associated with the specified mail merge field. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of elements contained in the collection. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns a dictionary iterator object that can be used to iterate over all items in the collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(String documentFieldName)](#remove-java.lang.String) | Removes a field mapping. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String) | Sets the name of the field in the data source associated with the specified mail merge field. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Adds a new field mapping.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |
| dataSourceFieldName | java.lang.String | Case-sensitive name of the field in the data source. |

### clear() {#clear}
```
public void clear()
```


Removes all elements from the collection.

### containsKey(String documentFieldName) {#containsKey-java.lang.String}
```
public boolean containsKey(String documentFieldName)
```


Determines whether a mapping from the specified field in the document exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |

**Returns:**
boolean - \{ true  if item is found in the collection; otherwise,  false .
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String}
```
public boolean containsValue(String dataSourceFieldName)
```


Determines whether a mapping from the specified field in the data source exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Case-sensitive name of the field in the data source. |

**Returns:**
boolean - \{ true  if item is found in the collection; otherwise,  false .
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
### get(String documentFieldName) {#get-java.lang.String}
```
public String get(String documentFieldName)
```


Gets the name of the field in the data source associated with the specified mail merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |

**Returns:**
java.lang.String - The name of the field in the data source associated with the specified mail merge field.
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


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
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


Returns a dictionary iterator object that can be used to iterate over all items in the collection.

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




### remove(String documentFieldName) {#remove-java.lang.String}
```
public void remove(String documentFieldName)
```


Removes a field mapping.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |

### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String}
```
public void set(String documentFieldName, String value)
```


Sets the name of the field in the data source associated with the specified mail merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| value | java.lang.String | The name of the field in the data source associated with the specified mail merge field. |

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

