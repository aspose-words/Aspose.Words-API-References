---
title: ViewOptions
second_title: Aspose.Words for Java API Reference
description: Provides various options that control how a document is shown in Microsoft Word.
type: docs
weight: 601
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

To learn more, visit the **Work with Options and Appearance of Word Documents** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getViewType()](#getViewType--) | Controls the view mode in Microsoft Word. |
| [setViewType(int value)](#setViewType-int-) | Controls the view mode in Microsoft Word. |
| [getZoomType()](#getZoomType--) | Gets a zoom value based on the size of the window. |
| [setZoomType(int value)](#setZoomType-int-) | Sets a zoom value based on the size of the window. |
| [getZoomPercent()](#getZoomPercent--) | Gets the percentage (between 10 and 500) at which you want to view your document. |
| [setZoomPercent(int value)](#setZoomPercent-int-) | Sets the percentage (between 10 and 500) at which you want to view your document. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries--) | Turns off display of the space between the top of the text and the top edge of the page. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean-) | Turns off display of the space between the top of the text and the top edge of the page. |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape--) | Controls display of the background shape in print layout view. |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean-) | Controls display of the background shape in print layout view. |
| [getFormsDesign()](#getFormsDesign--) | Specifies whether the document is in forms design mode. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean-) | Specifies whether the document is in forms design mode. |
### getViewType() {#getViewType--}
```
public int getViewType()
```


Controls the view mode in Microsoft Word.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Returns:**
int - The corresponding  int  value. The returned value is one of [ViewType](../../com.aspose.words/viewtype) constants.
### setViewType(int value) {#setViewType-int-}
```
public void setViewType(int value)
```


Controls the view mode in Microsoft Word.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ViewType](../../com.aspose.words/viewtype) constants. |

### getZoomType() {#getZoomType--}
```
public int getZoomType()
```


Gets a zoom value based on the size of the window.

**Returns:**
int - A zoom value based on the size of the window. The returned value is one of [ZoomType](../../com.aspose.words/zoomtype) constants.
### setZoomType(int value) {#setZoomType-int-}
```
public void setZoomType(int value)
```


Sets a zoom value based on the size of the window.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A zoom value based on the size of the window. The value must be one of [ZoomType](../../com.aspose.words/zoomtype) constants. |

### getZoomPercent() {#getZoomPercent--}
```
public int getZoomPercent()
```


Gets the percentage (between 10 and 500) at which you want to view your document.

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

**Returns:**
int - The percentage (between 10 and 500) at which you want to view your document.
### setZoomPercent(int value) {#setZoomPercent-int-}
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

### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries--}
```
public boolean getDoNotDisplayPageBoundaries()
```


Turns off display of the space between the top of the text and the top edge of the page.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean-}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Turns off display of the space between the top of the text and the top edge of the page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDisplayBackgroundShape() {#getDisplayBackgroundShape--}
```
public boolean getDisplayBackgroundShape()
```


Controls display of the background shape in print layout view.

**Returns:**
boolean - The corresponding  boolean  value.
### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean-}
```
public void setDisplayBackgroundShape(boolean value)
```


Controls display of the background shape in print layout view.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFormsDesign() {#getFormsDesign--}
```
public boolean getFormsDesign()
```


Specifies whether the document is in forms design mode.

Currently works only for documents in WordML format.

**Returns:**
boolean - The corresponding  boolean  value.
### setFormsDesign(boolean value) {#setFormsDesign-boolean-}
```
public void setFormsDesign(boolean value)
```


Specifies whether the document is in forms design mode.

Currently works only for documents in WordML format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

