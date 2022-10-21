---
title: DropDownItemCollection
second_title: Aspose.Words for Java API Reference
description: A collection of strings that represent all the items in a drop-down form field.
type: docs
weight: 135
url: /java/com.aspose.words/dropdownitemcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DropDownItemCollection implements Iterable
```

A collection of strings that represent all the items in a drop-down form field.

To learn more, visit the **Working with Fields** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(int index)](#get-int-) | Gets the element at the specified index. |
| [set(int index, String value)](#set-int-java.lang.String-) | Sets the element at the specified index. |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [add(String value)](#add-java.lang.String-) |  |
| [contains(String value)](#contains-java.lang.String-) | Determines whether the collection contains the specified value. |
| [indexOf(String value)](#indexOf-java.lang.String-) | Returns the zero-based index of the specified value in the collection. |
| [insert(int index, String value)](#insert-int-java.lang.String-) | Inserts a string into the collection at the specified index. |
| [remove(String name)](#remove-java.lang.String-) | Removes the specified value from the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a value at the specified index. |
| [clear()](#clear--) | Removes all elements from the collection. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### get(int index) {#get-int-}
```
public String get(int index)
```


Gets the element at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
java.lang.String - The element at the specified index.
### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


Sets the element at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | java.lang.String | The element at the specified index. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(String value) {#add-java.lang.String-}
```
public int add(String value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String |  |

**Returns:**
int
### contains(String value) {#contains-java.lang.String-}
```
public boolean contains(String value)
```


Determines whether the collection contains the specified value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Case-sensitive value to locate. |

**Returns:**
boolean - True if the item is found in the collection; otherwise, false.
### indexOf(String value) {#indexOf-java.lang.String-}
```
public int indexOf(String value)
```


Returns the zero-based index of the specified value in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The case-sensitive value to locate. |

**Returns:**
int - The zero based index. Negative value if not found.
### insert(int index, String value) {#insert-int-java.lang.String-}
```
public void insert(int index, String value)
```


Inserts a string into the collection at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index at which value is inserted. |
| value | java.lang.String | The string to insert. |

### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Removes the specified value from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-sensitive value to remove. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a value at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
