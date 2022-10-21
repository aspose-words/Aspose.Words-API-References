---
title: PdfLoadOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options when loading Pdf document into a  object.
type: docs
weight: 458
url: /java/com.aspose.words/pdfloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class PdfLoadOptions extends LoadOptions
```

Allows to specify additional options when loading Pdf document into a [Document](../../com.aspose.words/document) object.

To learn more, visit the **Specify Load Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getPageIndex()](#getPageIndex--) | Gets the 0-based index of the first page to read. |
| [setPageIndex(int value)](#setPageIndex-int-) | Sets the 0-based index of the first page to read. |
| [getPageCount()](#getPageCount--) | Gets the number of pages to read. |
| [setPageCount(int value)](#setPageCount-int-) | Sets the number of pages to read. |
| [getSkipPdfImages()](#getSkipPdfImages--) | Gets the flag indicating whether images must be skipped while loading PDF document. |
| [setSkipPdfImages(boolean value)](#setSkipPdfImages-boolean-) | Sets the flag indicating whether images must be skipped while loading PDF document. |
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Gets the 0-based index of the first page to read. Default is 0.

**Returns:**
int - The 0-based index of the first page to read.
### setPageIndex(int value) {#setPageIndex-int-}
```
public void setPageIndex(int value)
```


Sets the 0-based index of the first page to read. Default is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The 0-based index of the first page to read. |

### getPageCount() {#getPageCount--}
```
public int getPageCount()
```


Gets the number of pages to read. Default is MaxValue which means all pages of the document will be read.

**Returns:**
int - The number of pages to read.
### setPageCount(int value) {#setPageCount-int-}
```
public void setPageCount(int value)
```


Sets the number of pages to read. Default is MaxValue which means all pages of the document will be read.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number of pages to read. |

### getSkipPdfImages() {#getSkipPdfImages--}
```
public boolean getSkipPdfImages()
```


Gets the flag indicating whether images must be skipped while loading PDF document. Default is False.

**Returns:**
boolean - The flag indicating whether images must be skipped while loading PDF document.
### setSkipPdfImages(boolean value) {#setSkipPdfImages-boolean-}
```
public void setSkipPdfImages(boolean value)
```


Sets the flag indicating whether images must be skipped while loading PDF document. Default is False.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The flag indicating whether images must be skipped while loading PDF document. |

