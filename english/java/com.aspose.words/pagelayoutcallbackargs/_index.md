---
title: PageLayoutCallbackArgs
second_title: Aspose.Words for Java API Reference
description: An argument passed into
type: docs
weight: 439
url: /java/com.aspose.words/pagelayoutcallbackargs/
---

**Inheritance:**
java.lang.Object
```
public class PageLayoutCallbackArgs
```

An argument passed into [IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs)

To learn more, visit the [ Converting to Fixed-page Format ][Converting to Fixed-page Format] documentation article.


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDocument()](#getDocument) | Gets document. |
| [getEvent()](#getEvent) | Gets event. |
| [getPageIndex()](#getPageIndex) | Gets 0-based index of the page in the document this event relates to. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets document.

**Returns:**
[Document](../../com.aspose.words/document) - Document.
### getEvent() {#getEvent}
```
public int getEvent()
```


Gets event.

**Returns:**
int - Event. The returned value is one of [PageLayoutEvent](../../com.aspose.words/pagelayoutevent) constants.
### getPageIndex() {#getPageIndex}
```
public int getPageIndex()
```


Gets 0-based index of the page in the document this event relates to. Returns negative value if there is no associated page, or if page was removed during reflow.

**Returns:**
int - 0-based index of the page in the document this event relates to.
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

