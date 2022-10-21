---
title: PageSavingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  event.
type: docs
weight: 438
url: /java/com.aspose.words/pagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class PageSavingArgs
```

Provides data for the [IPageSavingCallback.pageSaving(com.aspose.words.PageSavingArgs)](../../com.aspose.words/ipagesavingcallback\#pageSaving-com.aspose.words.PageSavingArgs-) event.

To learn more, visit the **Programming with Documents** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getPageStream()](#getPageStream--) |  |
| [setPageStream(OutputStream value)](#setPageStream-java.io.OutputStream-) |  |
| [getKeepPageStreamOpen()](#getKeepPageStreamOpen--) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [setKeepPageStreamOpen(boolean value)](#setKeepPageStreamOpen-boolean-) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [getPageFileName()](#getPageFileName--) | Gets the file name where the document page will be saved to. |
| [setPageFileName(String value)](#setPageFileName-java.lang.String-) | Sets the file name where the document page will be saved to. |
| [getPageIndex()](#getPageIndex--) | Current page index. |
### getPageStream() {#getPageStream--}
```
public OutputStream getPageStream()
```




**Returns:**
java.io.OutputStream
### setPageStream(OutputStream value) {#setPageStream-java.io.OutputStream-}
```
public void setPageStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### getKeepPageStreamOpen() {#getKeepPageStreamOpen--}
```
public boolean getKeepPageStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a document page.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.PageSavingArgs.PageStream** property after writing a document page into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Returns:**
boolean - The corresponding  boolean  value.
### setKeepPageStreamOpen(boolean value) {#setKeepPageStreamOpen-boolean-}
```
public void setKeepPageStreamOpen(boolean value)
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a document page.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.PageSavingArgs.PageStream** property after writing a document page into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPageFileName() {#getPageFileName--}
```
public String getPageFileName()
```


Gets the file name where the document page will be saved to. If not specified then page file name and path will be generated automatically using original file name.

**Returns:**
java.lang.String - The file name where the document page will be saved to.
### setPageFileName(String value) {#setPageFileName-java.lang.String-}
```
public void setPageFileName(String value)
```


Sets the file name where the document page will be saved to. If not specified then page file name and path will be generated automatically using original file name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name where the document page will be saved to. |

### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Current page index.

**Returns:**
int - The corresponding  int  value.
