---
title: CustomDocumentProperties
linktitle: CustomDocumentProperties
second_title: Aspose.Words for Java API Reference
description: A collection of custom document properties in Java.
type: docs
weight: 102
url: /java/com.aspose.words/customdocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class CustomDocumentProperties extends DocumentPropertyCollection
```

A collection of custom document properties.

To learn more, visit the [ Work with Document Properties ][Work with Document Properties] documentation article.

Each [DocumentProperty](../../com.aspose.words/documentproperty/) object represents a custom property of a container document.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Methods

| Method | Description |
| --- | --- |
| [add(String name, boolean value)](#add-java.lang.String-boolean) | Creates a new custom document property of the [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN) data type. |
| [add(String name, double value)](#add-java.lang.String-double) | Creates a new custom document property of the [PropertyType.DOUBLE](../../com.aspose.words/propertytype/\#DOUBLE) data type. |
| [add(String name, int value)](#add-java.lang.String-int) | Creates a new custom document property of the [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER) data type. |
| [add(String name, String value)](#add-java.lang.String-java.lang.String) | Creates a new custom document property. |
| [add(String name, Date value)](#add-java.lang.String-java.util.Date) | Creates a new custom document property of the [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME) data type. |
| [addLinkToContent(String name, String linkSource)](#addLinkToContent-java.lang.String-java.lang.String) | Creates a new linked to content custom document property. |
| [clear()](#clear) | Removes all properties from the collection. |
| [contains(String name)](#contains-java.lang.String) | Returns  true  if a property with the specified name exists in the collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object by index. |
| [get(String name)](#get-java.lang.String) | Provides access to the collection items. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets number of items in the collection. |
| [hashCode()](#hashCode) |  |
| [indexOf(String name)](#indexOf-java.lang.String) | Gets the index of a property by name. |
| [iterator()](#iterator) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(String name)](#remove-java.lang.String) | Removes a property with the specified name from the collection. |
| [removeAt(int index)](#removeAt-int) | Removes a property at the specified index. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(String name, boolean value) {#add-java.lang.String-boolean}
```
public DocumentProperty add(String name, boolean value)
```


Creates a new custom document property of the [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN) data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | boolean | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, double value) {#add-java.lang.String-double}
```
public DocumentProperty add(String name, double value)
```


Creates a new custom document property of the [PropertyType.DOUBLE](../../com.aspose.words/propertytype/\#DOUBLE) data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | double | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, int value) {#add-java.lang.String-int}
```
public DocumentProperty add(String name, int value)
```


Creates a new custom document property of the [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER) data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | int | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, String value) {#add-java.lang.String-java.lang.String}
```
public DocumentProperty add(String name, String value)
```


Creates a new custom document property.  Creates a new custom document property of the [PropertyType.STRING](../../com.aspose.words/propertytype/\#STRING) data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | java.lang.String | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### add(String name, Date value) {#add-java.lang.String-java.util.Date}
```
public DocumentProperty add(String name, Date value)
```


Creates a new custom document property of the [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME) data type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| value | java.util.Date | The value of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object.
### addLinkToContent(String name, String linkSource) {#addLinkToContent-java.lang.String-java.lang.String}
```
public DocumentProperty addLinkToContent(String name, String linkSource)
```


Creates a new linked to content custom document property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the property. |
| linkSource | java.lang.String | The source of the property. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The newly created property object or  null  when the  linkSource  is invalid.
### clear() {#clear}
```
public void clear()
```


Removes all properties from the collection.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Returns  true  if a property with the specified name exists in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

**Returns:**
boolean - \{ true  if the property exists in the collection;  false  otherwise.
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
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the [DocumentProperty](../../com.aspose.words/documentproperty/) to retrieve. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Provides access to the collection items.  Returns a [DocumentProperty](../../com.aspose.words/documentproperty/) object by the name of the property.

Returns  null  if a property with the specified name is not found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property to retrieve. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
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


Gets number of items in the collection.

**Returns:**
int - Number of items in the collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Gets the index of a property by name.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

**Returns:**
int - The zero based index. Negative value if not found.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

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




### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Removes a property with the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The case-insensitive name of the property. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a property at the specified index.

**Note:**  In Java this method is slow because iterates over all nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero based index. |

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

