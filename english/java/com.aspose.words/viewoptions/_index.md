---
title: ViewOptions
second_title: Aspose.Words for Java API Reference
description: Provides various options that control how a document is shown in Microsoft Word.
type: docs
weight: 605
url: /java/com.aspose.words/viewoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Provides various options that control how a document is shown in Microsoft Word.

To learn more, visit the [ Work with Options and Appearance of Word Documents ][Work with Options and Appearance of Word Documents] documentation article.


[Work with Options and Appearance of Word Documents]: https://docs.aspose.com/words/java/work-with-word-document-options-and-appearance/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape) | Controls display of the background shape in print layout view. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries) | Turns off display of the space between the top of the text and the top edge of the page. |
| [getFormsDesign()](#getFormsDesign) | Specifies whether the document is in forms design mode. |
| [getViewType()](#getViewType) | Controls the view mode in Microsoft Word. |
| [getZoomPercent()](#getZoomPercent) | Gets the percentage (between 10 and 500) at which you want to view your document. |
| [getZoomType()](#getZoomType) | Gets a zoom value based on the size of the window. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean) | Controls display of the background shape in print layout view. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean) | Turns off display of the space between the top of the text and the top edge of the page. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean) | Specifies whether the document is in forms design mode. |
| [setViewType(int value)](#setViewType-int) | Controls the view mode in Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int) | Sets the percentage (between 10 and 500) at which you want to view your document. |
| [setZoomType(int value)](#setZoomType-int) | Sets a zoom value based on the size of the window. |
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
### getDisplayBackgroundShape() {#getDisplayBackgroundShape}
```
public boolean getDisplayBackgroundShape()
```


Controls display of the background shape in print layout view.

**Returns:**
boolean - The corresponding  boolean  value.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries}
```
public boolean getDoNotDisplayPageBoundaries()
```


Turns off display of the space between the top of the text and the top edge of the page.

**Returns:**
boolean - The corresponding  boolean  value.
### getFormsDesign() {#getFormsDesign}
```
public boolean getFormsDesign()
```


Specifies whether the document is in forms design mode.

Currently works only for documents in WordML format.

**Returns:**
boolean - The corresponding  boolean  value.
### getViewType() {#getViewType}
```
public int getViewType()
```


Controls the view mode in Microsoft Word.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Returns:**
int - The corresponding  int  value. The returned value is one of [ViewType](../../com.aspose.words/viewtype) constants.
### getZoomPercent() {#getZoomPercent}
```
public int getZoomPercent()
```


Gets the percentage (between 10 and 500) at which you want to view your document.

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Returns:**
int - The percentage (between 10 and 500) at which you want to view your document.
### getZoomType() {#getZoomType}
```
public int getZoomType()
```


Gets a zoom value based on the size of the window.

**Returns:**
int - A zoom value based on the size of the window. The returned value is one of [ZoomType](../../com.aspose.words/zoomtype) constants.
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




### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean}
```
public void setDisplayBackgroundShape(boolean value)
```


Controls display of the background shape in print layout view.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Turns off display of the space between the top of the text and the top edge of the page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean}
```
public void setFormsDesign(boolean value)
```


Specifies whether the document is in forms design mode.

Currently works only for documents in WordML format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setViewType(int value) {#setViewType-int}
```
public void setViewType(int value)
```


Controls the view mode in Microsoft Word.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ViewType](../../com.aspose.words/viewtype) constants. |

### setZoomPercent(int value) {#setZoomPercent-int}
```
public void setZoomPercent(int value)
```


Sets the percentage (between 10 and 500) at which you want to view your document.

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The percentage (between 10 and 500) at which you want to view your document. |

### setZoomType(int value) {#setZoomType-int}
```
public void setZoomType(int value)
```


Sets a zoom value based on the size of the window.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A zoom value based on the size of the window. The value must be one of [ZoomType](../../com.aspose.words/zoomtype) constants. |

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

