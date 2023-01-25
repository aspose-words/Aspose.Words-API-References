---
title: TabStopCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent custom tabs for a paragraph or a style.
type: docs
weight: 551
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

To learn more, visit the [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] documentation article.

In Microsoft Word documents, a tab stop can be defined in the properties of a paragraph style or directly in the properties of a paragraph. A style can be based on another style. Therefore, the complete set of tab stops for a given object is a combination of tab stops defined directly on this object and tab stops inherited from the parent styles.

In Aspose.Words, when you obtain a [TabStopCollection](../../com.aspose.words/tabstopcollection) for a paragraph or a style, it contains only the custom tab stops defined directly for this paragraph or style. The collection does not include tab stops defined in the parent styles or default tab stops.


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Methods

| Method | Description |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop) | Adds or replaces a tab stop in the collection. |
| [add(double position, int alignment, int leader)](#add-double-int-int) |  |
| [after(double position)](#after-double) | Gets a first tab stop to the right of the specified position. |
| [before(double position)](#before-double) | Gets a first tab stop to the left of the specified position. |
| [clear()](#clear) | Deletes all tab stop positions. |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection) | Determines whether the specified [TabStopCollection](../../com.aspose.words/tabstopcollection) is equal in value to the current [TabStopCollection](../../com.aspose.words/tabstopcollection). |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [get(double position)](#get-double) | Gets a tab stop at the specified position. |
| [get(int index)](#get-int) | Retrieves a tab stop from the collection. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of tab stops in the collection. |
| [getIndexByPosition(double position)](#getIndexByPosition-double) | Gets the index of a tab stop with the specified position in points. |
| [getPositionByIndex(int index)](#getPositionByIndex-int) | Gets the position (in points) of the tab stop at the specified index. |
| [hashCode()](#hashCode) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [removeByIndex(int index)](#removeByIndex-int) | Removes a tab stop at the specified index from the collection. |
| [removeByPosition(double position)](#removeByPosition-double) | Removes a tab stop at the specified position from the collection. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop}
```
public void add(TabStop tabStop)
```


Adds or replaces a tab stop in the collection.

If a tab stop already exists at the specified position, it is replaced.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop) | A tab stop object to add. |

### add(double position, int alignment, int leader) {#add-double-int-int}
```
public void add(double position, int alignment, int leader)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### after(double position) {#after-double}
```
public TabStop after(double position)
```


Gets a first tab stop to the right of the specified position.

Skips tab stops with [TabStop.getAlignment()](../../com.aspose.words/tabstop\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop\#setAlignment-int) set to [TabAlignment.BAR](../../com.aspose.words/tabalignment\#BAR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - A tab stop object or  null  if a suitable tab stop was not found.
### before(double position) {#before-double}
```
public TabStop before(double position)
```


Gets a first tab stop to the left of the specified position.

Skips tab stops with [TabStop.getAlignment()](../../com.aspose.words/tabstop\#getAlignment) / [TabStop.setAlignment(int)](../../com.aspose.words/tabstop\#setAlignment-int) set to [TabAlignment.BAR](../../com.aspose.words/tabalignment\#BAR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The reference position (in points). |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - A tab stop object or  null  if a suitable tab stop was not found.
### clear() {#clear}
```
public void clear()
```


Deletes all tab stop positions.

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection}
```
public boolean equals(TabStopCollection rhs)
```


Determines whether the specified [TabStopCollection](../../com.aspose.words/tabstopcollection) is equal in value to the current [TabStopCollection](../../com.aspose.words/tabstopcollection).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
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
### get(double position) {#get-double}
```
public TabStop get(double position)
```


Gets a tab stop at the specified position. Returns  null  if no tab stop is found at the specified position.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop. |

**Returns:**
[TabStop](../../com.aspose.words/tabstop) - A tab stop at the specified position.
### get(int index) {#get-int}
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


Gets the number of tab stops in the collection.

**Returns:**
int - The number of tab stops in the collection.
### getIndexByPosition(double position) {#getIndexByPosition-double}
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
### getPositionByIndex(int index) {#getPositionByIndex-int}
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
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isInheritedComplexAttr() {#isInheritedComplexAttr}
```
public boolean isInheritedComplexAttr()
```




**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### removeByIndex(int index) {#removeByIndex-int}
```
public void removeByIndex(int index)
```


Removes a tab stop at the specified index from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection of tab stops. |

### removeByPosition(double position) {#removeByPosition-double}
```
public void removeByPosition(double position)
```


Removes a tab stop at the specified position from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| position | double | The position (in points) of the tab stop to remove. |

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

