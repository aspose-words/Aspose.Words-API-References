---
title: VariableCollection
second_title: Aspose.Words for Java API Reference
description: A collection of document variables.
type: docs
weight: 592
url: /java/com.aspose.words/variablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VariableCollection implements Iterable
```

A collection of document variables.

To learn more, visit the **Work with Document Properties** documentation article.

Variable names and values are strings.

Variable names are case-insensitive.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(String name)](#get-java.lang.String-) | Provides access to the collection items. |
| [set(String name, String value)](#set-java.lang.String-java.lang.String-) | Provides access to the collection items. |
| [get(int index)](#get-int-) | Gets a document variable at the specified index. |
| [set(int index, String value)](#set-int-java.lang.String-) | Sets a document variable at the specified index. |
| [iterator()](#iterator--) | Returns an enumerator object that can be used to iterate over all variable in the collection. |
| [add(String name, String value)](#add-java.lang.String-java.lang.String-) | Adds a document variable to the collection. |
| [contains(String name)](#contains-java.lang.String-) | Determines whether the collection contains a document variable with the given name. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | Returns the zero-based index of the specified document variable in the collection. |
| [remove(String name)](#remove-java.lang.String-) | Removes a document variable with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a document variable at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(String name) {#get-java.lang.String-}
```
public String get(String name)
```


Provides access to the collection items.  Gets or a sets a document variable by the case-insensitive name. null values are not allowed as a right hand side of the assignment and will be replaced by empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### set(String name, String value) {#set-java.lang.String-java.lang.String-}
```
public void set(String name, String value)
```


Provides access to the collection items.  Gets or a sets a document variable by the case-insensitive name. null values are not allowed as a right hand side of the assignment and will be replaced by empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |
| value | java.lang.String | The corresponding java.lang.String value. |

### get(int index) {#get-int-}
```
public String get(int index)
```


Gets a document variable at the specified index. null values are not allowed as a right hand side of the assignment and will be replaced by empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the document variable. |

**Returns:**
java.lang.String - A document variable at the specified index.
### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


Sets a document variable at the specified index. null values are not allowed as a right hand side of the assignment and will be replaced by empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the document variable. |
| value | java.lang.String | A document variable at the specified index. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object that can be used to iterate over all variable in the collection.

**Returns:**
java.util.Iterator
### add(String name, String value) {#add-java.lang.String-java.lang.String-}
```
public void add(String name, String value)
```


Adds a document variable to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the variable to add. |
| value | java.lang.String | The value of the variable. The value cannot be null, if value is null empty string will be used instead. |

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Determines whether the collection contains a document variable with the given name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the document variable to locate. |

**Returns:**
boolean - True if item is found in the collection; otherwise, false.
### indexOfKey(String name) {#indexOfKey-java.lang.String-}
```
public int indexOfKey(String name)
```


Returns the zero-based index of the specified document variable in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the variable. |

**Returns:**
int - The zero based index. Negative value if not found.
### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Removes a document variable with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the variable. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a document variable at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

