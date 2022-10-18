---
title: TabStopCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent custom tabs for a paragraph or a style.
type: docs
weight: 547
url: /java/com.aspose.words/tabstopcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

A collection of [TabStop](../../com.aspose.words/tabstop) objects that represent custom tabs for a paragraph or a style.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph style or directly in the properties of a paragraph. A style can be based on another style. Therefore, the complete set of tab stops for a given object is a combination of tab stops defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a **TabStops** collection for a paragraph or a style, it contains only the custom tab stops defined directly for this paragraph or style. The collection does not include tab stops defined in the parent styles or default tab stops.
## Methods

| Method | Description |
| --- | --- |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection-) | Determines whether the specified TabStopCollection is equal in value to the current TabStopCollection. |
| [equals(Object obj)](#equals-java.lang.Object-) | Determines whether the specified object is equal in value to the current object. |
| [hashCode()](#hashCode--) |  |
| [getCount()](#getCount--) | Gets the number of tab stops in the collection. |
| [get(int index)](#get-int-) | Retrieves a tab stop from the collection. |
| [get(double position)](#get-double-) | Gets a tab stop at the specified position. |
| [clear()](#clear--) | Deletes all tab stop positions. |
| [getPositionByIndex(int index)](#getPositionByIndex-int-) | Gets the position (in points) of the tab stop at the specified index. |
| [getIndexByPosition(double position)](#getIndexByPosition-double-) | Gets the index of a tab stop with the specified position in points. |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop-) | Adds or replaces a tab stop in the collection. |
| [add(double position, int alignment, int leader)](#add-double-int-int-) |  |
| [removeByPosition(double position)](#removeByPosition-double-) | Removes a tab stop at the specified position from the collection. |
| [removeByIndex(int index)](#removeByIndex-int-) | Removes a tab stop at the specified index from the collection. |
| [after(double position)](#after-double-) | Gets a first tab stop to the right of the specified position. |
| [before(double position)](#before-double-) | Gets a first tab stop to the left of the specified position. |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection-}
```
public boolean equals(TabStopCollection rhs)
```


Determines whether the specified TabStopCollection is equal in value to the current TabStopCollection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of tab stops in the collection.

**Returns:**
int - The number of tab stops in the collection.
### get(int index) {#get-int-}
```
public TabStop get(int index)
```


Retrieves a tab stop from the collection.  Gets a tab stop at the given index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - The corresponding [TabStop](../../com.aspose.words/tabstop) value.
### get(double position) {#get-double-}
```
public TabStop get(double position)
```


Gets a tab stop at the specified position. Returns null if no tab stop is found at the specified position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - A tab stop at the specified position.
### clear() {#clear--}
```
public void clear()
```


Deletes all tab stop positions.

### getPositionByIndex(int index) {#getPositionByIndex-int-}
```
public double getPositionByIndex(int index)
```


Gets the position (in points) of the tab stop at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

**Returns:**
double - The position of the tab stop.
### getIndexByPosition(double position) {#getIndexByPosition-double-}
```
public int getIndexByPosition(double position)
```


Gets the index of a tab stop with the specified position in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |

**Returns:**
int
### add(TabStop tabStop) {#add-com.aspose.words.TabStop-}
```
public void add(TabStop tabStop)
```


Adds or replaces a tab stop in the collection.

If a tab stop already exists at the specified position, it is replaced.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop) | A tab stop object to add. |

### add(double position, int alignment, int leader) {#add-double-int-int-}
```
public void add(double position, int alignment, int leader)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### removeByPosition(double position) {#removeByPosition-double-}
```
public void removeByPosition(double position)
```


Removes a tab stop at the specified position from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop to remove. |

### removeByIndex(int index) {#removeByIndex-int-}
```
public void removeByIndex(int index)
```


Removes a tab stop at the specified index from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

### after(double position) {#after-double-}
```
public TabStop after(double position)
```


Gets a first tab stop to the right of the specified position.

Skips tab stops with **Alignment** set to  TabAlignment.Bar .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - A tab stop object or null if a suitable tab stop was not found.
### before(double position) {#before-double-}
```
public TabStop before(double position)
```


Gets a first tab stop to the left of the specified position.

Skips tab stops with **Alignment** set to  TabAlignment.Bar .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - A tab stop object or null if a suitable tab stop was not found.
### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
