---
title: GradientStopCollection
second_title: Aspose.Words for Java API Reference
description: Contains a collection of  objects.
type: docs
weight: 309
url: /java/com.aspose.words/gradientstopcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class GradientStopCollection implements Iterable
```

Contains a collection of [GradientStop](../../com.aspose.words/gradientstop) objects.

To learn more, visit the **Working with Graphic Elements** documentation article.

You do not create instances of this class directly. Use the [Fill.getGradientStops()](../../com.aspose.words/fill\#getGradientStops--) property to access gradient stops of fill objects.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Gets a [GradientStop](../../com.aspose.words/gradientstop) object in the collection. |
| [set(int index, GradientStop value)](#set-int-com.aspose.words.GradientStop-) | Sets a [GradientStop](../../com.aspose.words/gradientstop) object in the collection. |
| [insert(int index, GradientStop gradientStop)](#insert-int-com.aspose.words.GradientStop-) | Inserts a [GradientStop](../../com.aspose.words/gradientstop) to the collection at a specified index. |
| [add(GradientStop gradientStop)](#add-com.aspose.words.GradientStop-) | Adds a specified [GradientStop](../../com.aspose.words/gradientstop) to a gradient. |
| [removeAt(int index)](#removeAt-int-) | Removes a [GradientStop](../../com.aspose.words/gradientstop) from the collection at a specified index. |
| [remove(GradientStop gradientStop)](#remove-com.aspose.words.GradientStop-) | Removes a specified [GradientStop](../../com.aspose.words/gradientstop) from the collection. |
| [iterator()](#iterator--) | Returns an enumerator that iterates through the collection. |
| [getCount()](#getCount--) | Gets an integer value indicating the number of items in the collection. |
### get(int index) {#get-int-}
```
public GradientStop get(int index)
```


Gets a [GradientStop](../../com.aspose.words/gradientstop) object in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop) - A [GradientStop](../../com.aspose.words/gradientstop) object in the collection.
### set(int index, GradientStop value) {#set-int-com.aspose.words.GradientStop-}
```
public void set(int index, GradientStop value)
```


Sets a [GradientStop](../../com.aspose.words/gradientstop) object in the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [GradientStop](../../com.aspose.words/gradientstop) | A [GradientStop](../../com.aspose.words/gradientstop) object in the collection. |

### insert(int index, GradientStop gradientStop) {#insert-int-com.aspose.words.GradientStop-}
```
public GradientStop insert(int index, GradientStop gradientStop)
```


Inserts a [GradientStop](../../com.aspose.words/gradientstop) to the collection at a specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop) |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop)
### add(GradientStop gradientStop) {#add-com.aspose.words.GradientStop-}
```
public GradientStop add(GradientStop gradientStop)
```


Adds a specified [GradientStop](../../com.aspose.words/gradientstop) to a gradient.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop) |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop)
### removeAt(int index) {#removeAt-int-}
```
public GradientStop removeAt(int index)
```


Removes a [GradientStop](../../com.aspose.words/gradientstop) from the collection at a specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop) - Removed [GradientStop](../../com.aspose.words/gradientstop).
### remove(GradientStop gradientStop) {#remove-com.aspose.words.GradientStop-}
```
public boolean remove(GradientStop gradientStop)
```


Removes a specified [GradientStop](../../com.aspose.words/gradientstop) from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop) |  |

**Returns:**
boolean - True if gradient stop was successfully removed, otherwise false.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator that iterates through the collection.

**Returns:**
java.util.Iterator
### getCount() {#getCount--}
```
public int getCount()
```


Gets an integer value indicating the number of items in the collection.

**Returns:**
int - An integer value indicating the number of items in the collection.
