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
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getKeepPageStreamOpen()](#getKeepPageStreamOpen--) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [getPageFileName()](#getPageFileName--) | Gets the file name where the document page will be saved to. |
| [getPageIndex()](#getPageIndex--) | Current page index. |
| [getPageStream()](#getPageStream--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setKeepPageStreamOpen(boolean value)](#setKeepPageStreamOpen-boolean-) | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [setPageFileName(String value)](#setPageFileName-java.lang.String-) | Sets the file name where the document page will be saved to. |
| [setPageStream(OutputStream value)](#setPageStream-java.io.OutputStream-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getKeepPageStreamOpen() {#getKeepPageStreamOpen--}
```
public boolean getKeepPageStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving a document page.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.PageSavingArgs.PageStream** property after writing a document page into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Returns:**
boolean - The corresponding  boolean  value.
### getPageFileName() {#getPageFileName--}
```
public String getPageFileName()
```


Gets the file name where the document page will be saved to. If not specified then page file name and path will be generated automatically using original file name.

**Returns:**
java.lang.String - The file name where the document page will be saved to.
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Current page index.

**Returns:**
int - The corresponding  int  value.
### getPageStream() {#getPageStream--}
```
public OutputStream getPageStream()
```




**Returns:**
java.io.OutputStream
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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

### setPageFileName(String value) {#setPageFileName-java.lang.String-}
```
public void setPageFileName(String value)
```


Sets the file name where the document page will be saved to. If not specified then page file name and path will be generated automatically using original file name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name where the document page will be saved to. |

### setPageStream(OutputStream value) {#setPageStream-java.io.OutputStream-}
```
public void setPageStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

