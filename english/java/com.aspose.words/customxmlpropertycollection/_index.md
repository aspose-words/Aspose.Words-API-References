---
title: CustomXmlPropertyCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of custom XML attributes or smart tag properties.
type: docs
weight: 107
url: /java/com.aspose.words/customxmlpropertycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class CustomXmlPropertyCollection implements Iterable
```

Represents a collection of custom XML attributes or smart tag properties.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

Items are [CustomXmlProperty](../../com.aspose.words/customxmlproperty) objects.
## Methods

| Method | Description |
| --- | --- |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [get(String name)](#get-java.lang.String-) | Provides access to the collection items. |
| [get(int index)](#get-int-) | Gets a property at the specified index. |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [add(CustomXmlProperty property)](#add-com.aspose.words.CustomXmlProperty-) | Adds a property to the collection. |
| [contains(String name)](#contains-java.lang.String-) | Determines whether the collection contains a property with the given name. |
| [indexOfKey(String name)](#indexOfKey-java.lang.String-) | Returns the zero-based index of the specified property in the collection. |
| [remove(String name)](#remove-java.lang.String-) | Removes a property with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int-) | Removes a property at the specified index. |
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
public CustomXmlProperty get(String name)
```


Provides access to the collection items.  Gets a property with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-sensitive name of the property to locate. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty) - The corresponding [CustomXmlProperty](../../com.aspose.words/customxmlproperty) value.
### get(int index) {#get-int-}
```
public CustomXmlProperty get(int index)
```


Gets a property at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the property. |

**Returns:**
[CustomXmlProperty](../../com.aspose.words/customxmlproperty) - A property at the specified index.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### add(CustomXmlProperty property) {#add-com.aspose.words.CustomXmlProperty-}
```
public void add(CustomXmlProperty property)
```


Adds a property to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| property | [CustomXmlProperty](../../com.aspose.words/customxmlproperty) | The property to add. |

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Determines whether the collection contains a property with the given name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-sensitive name of the property to locate. |

**Returns:**
boolean - True if the item is found in the collection; otherwise, false.
### indexOfKey(String name) {#indexOfKey-java.lang.String-}
```
public int indexOfKey(String name)
```


Returns the zero-based index of the specified property in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-sensitive name of the property. |

**Returns:**
int - The zero based index. Negative value if not found.
### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Removes a property with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-sensitive name of the property. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a property at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

