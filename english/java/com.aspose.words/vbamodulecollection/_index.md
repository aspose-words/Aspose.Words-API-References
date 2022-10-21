---
title: VbaModuleCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of  objects.
type: docs
weight: 594
url: /java/com.aspose.words/vbamodulecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class VbaModuleCollection implements Iterable
```

Represents a collection of [VbaModule](../../com.aspose.words/vbamodule) objects.

To learn more, visit the **Working with VBA Macros** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [add(VbaModule vbaModule)](#add-com.aspose.words.VbaModule-) | Adds a module to the collection. |
| [get(int index)](#get-int-) | Retrieves a [VbaModule](../../com.aspose.words/vbamodule) object by index. |
| [get(String name)](#get-java.lang.String-) | Retrieves a [VbaModule](../../com.aspose.words/vbamodule) object by name, or Null if not found. |
| [getCount()](#getCount--) | Returns the number of VBA modules in the collection. |
| [remove(VbaModule module)](#remove-com.aspose.words.VbaModule-) | Removes the specified module from the collection. |
| [iterator()](#iterator--) |  |
### add(VbaModule vbaModule) {#add-com.aspose.words.VbaModule-}
```
public void add(VbaModule vbaModule)
```


Adds a module to the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| vbaModule | [VbaModule](../../com.aspose.words/vbamodule) |  |

### get(int index) {#get-int-}
```
public VbaModule get(int index)
```


Retrieves a [VbaModule](../../com.aspose.words/vbamodule) object by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the module to retrieve. |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule) - The corresponding [VbaModule](../../com.aspose.words/vbamodule) value.
### get(String name) {#get-java.lang.String-}
```
public VbaModule get(String name)
```


Retrieves a [VbaModule](../../com.aspose.words/vbamodule) object by name, or Null if not found.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[VbaModule](../../com.aspose.words/vbamodule) - The corresponding [VbaModule](../../com.aspose.words/vbamodule) value.
### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of VBA modules in the collection.

**Returns:**
int - The number of VBA modules in the collection.
### remove(VbaModule module) {#remove-com.aspose.words.VbaModule-}
```
public void remove(VbaModule module)
```


Removes the specified module from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| module | [VbaModule](../../com.aspose.words/vbamodule) | The module to remove. |

### iterator() {#iterator--}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
