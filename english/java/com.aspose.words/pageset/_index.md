---
title: PageSet
second_title: Aspose.Words for Java API Reference
description: Describes a random set of pages.
type: docs
weight: 442
url: /java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object
```
public class PageSet
```

Describes a random set of pages.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Constructors

| Constructor | Description |
| --- | --- |
| [PageSet(int page)](#PageSet-int) | Creates an one-page set based on exact page index. |
| [PageSet(int[] pages)](#PageSet-int...) | Creates a page set based on exact page indices. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...) | Creates a page set based on ranges. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAll()](#getAll) | Gets a set with all the pages of the document in their original order. |
| [getClass()](#getClass) |  |
| [getEven()](#getEven) | Gets a set with all the even pages of the document in their original order. |
| [getOdd()](#getOdd) | Gets a set with all the odd pages of the document in their original order. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### PageSet(int page) {#PageSet-int}
```
public PageSet(int page)
```


Creates an one-page set based on exact page index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| page | int | Zero-based index of the page. If a page is encountered that is not in the document, an exception will be thrown during rendering.  means the last page in the document. |

### PageSet(int[] pages) {#PageSet-int...}
```
public PageSet(int[] pages)
```


Creates a page set based on exact page indices.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pages | int[] | Zero-based indices of pages. If a page is encountered that is not in the document, an exception will be thrown during rendering.  means the last page in the document. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...}
```
public PageSet(PageRange[] ranges)
```


Creates a page set based on ranges.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange) | Array of page ranges. If a range is encountered that starts after the last page in the document, an exception will be thrown during rendering. All ranges that end after the last page are truncated to fit in the document. |

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
### getAll() {#getAll}
```
public static PageSet getAll()
```


Gets a set with all the pages of the document in their original order.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - A set with all the pages of the document in their original order.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getEven() {#getEven}
```
public static PageSet getEven()
```


Gets a set with all the even pages of the document in their original order. Even pages have odd indices since page indices are zero-based.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - A set with all the even pages of the document in their original order.
### getOdd() {#getOdd}
```
public static PageSet getOdd()
```


Gets a set with all the odd pages of the document in their original order. Odd pages have even indices since page indices are zero-based.

**Returns:**
[PageSet](../../com.aspose.words/pageset) - A set with all the odd pages of the document in their original order.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




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

