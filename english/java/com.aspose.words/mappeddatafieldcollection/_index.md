---
title: MappedDataFieldCollection
second_title: Aspose.Words for Java API Reference
description: Allows to automatically map between names of fields in your data source and names of mail merge fields in the document.
type: docs
weight: 387
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

To learn more, visit the **Mail Merge and Reporting** documentation article.

This is implemented as a collection of string keys into string values. The keys are the names of mail merge fields in the document and the values are the names of fields in your data source.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(String documentFieldName)](#get-java.lang.String-) | Gets the name of the field in the data source associated with the specified mail merge field. |
| [set(String documentFieldName, String value)](#set-java.lang.String-java.lang.String-) | Sets the name of the field in the data source associated with the specified mail merge field. |
| [iterator()](#iterator--) | Returns a dictionary iterator object that can be used to iterate over all items in the collection. |
| [add(String documentFieldName, String dataSourceFieldName)](#add-java.lang.String-java.lang.String-) | Adds a new field mapping. |
| [containsKey(String documentFieldName)](#containsKey-java.lang.String-) | Determines whether a mapping from the specified field in the document exists in the collection. |
| [containsValue(String dataSourceFieldName)](#containsValue-java.lang.String-) | Determines whether a mapping from the specified field in the data source exists in the collection. |
| [remove(String documentFieldName)](#remove-java.lang.String-) | Removes a field mapping. |
| [clear()](#clear--) | Removes all elements from the collection. |
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(String documentFieldName) {#get-java.lang.String-}
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
### set(String documentFieldName, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String documentFieldName, String value)
```


Sets the name of the field in the data source associated with the specified mail merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String |  |
| value | java.lang.String | The name of the field in the data source associated with the specified mail merge field. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns a dictionary iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(String documentFieldName, String dataSourceFieldName) {#add-java.lang.String-java.lang.String-}
```
public void add(String documentFieldName, String dataSourceFieldName)
```


Adds a new field mapping.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |
| dataSourceFieldName | java.lang.String | Case-sensitive name of the field in the data source. |

### containsKey(String documentFieldName) {#containsKey-java.lang.String-}
```
public boolean containsKey(String documentFieldName)
```


Determines whether a mapping from the specified field in the document exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |

**Returns:**
boolean - True if item is found in the collection; otherwise, false.
### containsValue(String dataSourceFieldName) {#containsValue-java.lang.String-}
```
public boolean containsValue(String dataSourceFieldName)
```


Determines whether a mapping from the specified field in the data source exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSourceFieldName | java.lang.String | Case-sensitive name of the field in the data source. |

**Returns:**
boolean - True if item is found in the collection; otherwise, false.
### remove(String documentFieldName) {#remove-java.lang.String-}
```
public void remove(String documentFieldName)
```


Removes a field mapping.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentFieldName | java.lang.String | Case-sensitive name of the mail merge field in the document. |

### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

