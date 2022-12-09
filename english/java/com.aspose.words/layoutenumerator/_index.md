---
title: LayoutEnumerator
second_title: Aspose.Words for Java API Reference
description: Enumerates page layout entities of a document.
type: docs
weight: 362
url: /java/com.aspose.words/layoutenumerator/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEnumerator
```

Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of [LayoutCollector.getEntity(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEntity-com.aspose.words.Node) and [getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object) move to the entity which corresponds to a document node.

To learn more, visit the [ Converting to Fixed-page Format ][Converting to Fixed-page Format] documentation article.


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Constructors

| Constructor | Description |
| --- | --- |
| [LayoutEnumerator(Document document)](#LayoutEnumerator-com.aspose.words.Document) | Initializes new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(String key)](#get-java.lang.String) | Gets a named property of the entity. |
| [getClass()](#getClass) |  |
| [getCurrent()](#getCurrent) | Gets current position in the page layout model. |
| [getDocument()](#getDocument) | Gets document this instance enumerates. |
| [getKind()](#getKind) | Gets the kind of the current entity. |
| [getPageIndex()](#getPageIndex) | Gets the 1-based index of a page which contains the current entity. |
| [getRectangle()](#getRectangle) | Returns the bounding rectangle of the current entity relative to the page top left corner (in points). |
| [getText()](#getText) | Gets text of the current span entity. |
| [getType()](#getType) | Gets the type of the current entity. |
| [hashCode()](#hashCode) |  |
| [moveFirstChild()](#moveFirstChild) | Moves to the first child entity. |
| [moveLastChild()](#moveLastChild) | Moves to the last child entity. |
| [moveNext()](#moveNext) | Moves to the next sibling entity in visual order. |
| [moveNextLogical()](#moveNextLogical) | Moves to the next sibling entity in a logical order. |
| [moveParent()](#moveParent) | Moves to the parent entity. |
| [moveParent(int types)](#moveParent-int) |  |
| [movePrevious()](#movePrevious) | Moves to the previous sibling entity. |
| [movePreviousLogical()](#movePreviousLogical) | Moves to the previous sibling entity in a logical order. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [reset()](#reset) | Moves the enumerator to the first page of the document. |
| [setCurrent(Object value)](#setCurrent-java.lang.Object) | Sets current position in the page layout model. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### LayoutEnumerator(Document document) {#LayoutEnumerator-com.aspose.words.Document}
```
public LayoutEnumerator(Document document)
```


Initializes new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | A document whose page layout model to enumerate.

If page layout model of the document hasn't been built the enumerator calls [Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout) to build it.

Whenever document is updated and new page layout model is created, a new enumerator must be used to access it. |

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
### get(String key) {#get-java.lang.String}
```
public Object get(String key)
```


Gets a named property of the entity.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | java.lang.String | A name of the property (case-sensitive). |

**Returns:**
java.lang.Object - Null if property is not available, otherwise value of the property. This is currently used to get font properties of spans. See [Font](../../com.aspose.words/font) class for possible properties names. Not all properties are supported.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCurrent() {#getCurrent}
```
public Object getCurrent()
```


Gets current position in the page layout model. This property returns an opaque object which corresponds to the current layout entity.

**Returns:**
java.lang.Object - Current position in the page layout model.
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets document this instance enumerates.

**Returns:**
[Document](../../com.aspose.words/document) - Document this instance enumerates.
### getKind() {#getKind}
```
public String getKind()
```


Gets the kind of the current entity. This can be an empty string but never  null . This is a more specific type of the current entity, e.g. bookmark span has [LayoutEntityType.SPAN](../../com.aspose.words/layoutentitytype\#SPAN) type and may have either a BOOKMARKSTART or BOOKMARKEND kind.

**Returns:**
java.lang.String - The kind of the current entity.
### getPageIndex() {#getPageIndex}
```
public int getPageIndex()
```


Gets the 1-based index of a page which contains the current entity.

**Returns:**
int - The 1-based index of a page which contains the current entity.
### getRectangle() {#getRectangle}
```
public Rectangle2D.Float getRectangle()
```


Returns the bounding rectangle of the current entity relative to the page top left corner (in points).

**Returns:**
java.awt.geom.Rectangle2D.Float - The bounding rectangle of the current entity relative to the page top left corner (in points).
### getText() {#getText}
```
public String getText()
```


Gets text of the current span entity. Throws for other entity types.

**Returns:**
java.lang.String - Text of the current span entity.
### getType() {#getType}
```
public int getType()
```


Gets the type of the current entity.

**Returns:**
int - The type of the current entity. The returned value is a bitwise combination of [LayoutEntityType](../../com.aspose.words/layoutentitytype) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### moveFirstChild() {#moveFirstChild}
```
public boolean moveFirstChild()
```


Moves to the first child entity.

**Returns:**
boolean
### moveLastChild() {#moveLastChild}
```
public boolean moveLastChild()
```


Moves to the last child entity.

**Returns:**
boolean
### moveNext() {#moveNext}
```
public boolean moveNext()
```


Moves to the next sibling entity in visual order. When iterating lines of a paragraph broken across pages this method will not move to the next page but rather move to the next entity on the same page.

**Returns:**
boolean
### moveNextLogical() {#moveNextLogical}
```
public boolean moveNextLogical()
```


Moves to the next sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the next line even if it resides on another page. Note that all [LayoutEntityType.SPAN](../../com.aspose.words/layoutentitytype\#SPAN) entities are linked together thus if [getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object) entity is span repeated calling of this method will iterates complete story of the document.

**Returns:**
boolean
### moveParent() {#moveParent}
```
public boolean moveParent()
```


Moves to the parent entity.

**Returns:**
boolean
### moveParent(int types) {#moveParent-int}
```
public boolean moveParent(int types)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| types | int |  |

**Returns:**
boolean
### movePrevious() {#movePrevious}
```
public boolean movePrevious()
```


Moves to the previous sibling entity.

**Returns:**
boolean
### movePreviousLogical() {#movePreviousLogical}
```
public boolean movePreviousLogical()
```


Moves to the previous sibling entity in a logical order. When iterating lines of a paragraph broken across pages this method will move to the previous line even if it resides on another page. Note that all [LayoutEntityType.SPAN](../../com.aspose.words/layoutentitytype\#SPAN) entities are linked together thus if [getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object) entity is span repeated calling of this method will iterates complete story of the document.

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




### reset() {#reset}
```
public void reset()
```


Moves the enumerator to the first page of the document.

### setCurrent(Object value) {#setCurrent-java.lang.Object}
```
public void setCurrent(Object value)
```


Sets current position in the page layout model. This property returns an opaque object which corresponds to the current layout entity.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | Current position in the page layout model. |

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

