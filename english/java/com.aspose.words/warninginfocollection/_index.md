---
title: WarningInfoCollection
second_title: Aspose.Words for Java API Reference
description: Represents a typed collection of  objects.
type: docs
weight: 605
url: /java/com.aspose.words/warninginfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

Represents a typed collection of [WarningInfo](../../com.aspose.words/warninginfo) objects.

To learn more, visit the **Programming with Documents** documentation article.

You can use this collection object as the simplest form of [IWarningCallback](../../com.aspose.words/iwarningcallback) implementation to gather all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it to the [LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions\#getWarningCallback--) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions\#setWarningCallback-com.aspose.words.IWarningCallback-) or [DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase\#getWarningCallback--) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase\#setWarningCallback-com.aspose.words.IWarningCallback-) property.
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear--) | Removes all elements from the collection. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Gets an item at the specified index. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo-) | Implements the [IWarningCallback](../../com.aspose.words/iwarningcallback) interface. |
### clear() {#clear--}
```
public void clear()
```


Removes all elements from the collection.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### get(int index) {#get-int-}
```
public WarningInfo get(int index)
```


Gets an item at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the item. |

**Returns:**
[WarningInfo](../../com.aspose.words/warninginfo) - An item at the specified index.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo-}
```
public void warning(WarningInfo info)
```


Implements the [IWarningCallback](../../com.aspose.words/iwarningcallback) interface. Adds a warning to this collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo) |  |

