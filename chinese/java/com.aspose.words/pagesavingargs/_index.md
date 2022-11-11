---
title: PageSavingArgs
second_title: Aspose.Words for Java API Reference
description: 为事件提供数据。
type: docs
weight: 438
url: /zh/java/com.aspose.words/pagesavingargs/
---

**遗产:**
java.lang.Object
```
public class PageSavingArgs
```

提供数据为[IPageSavingCallback.pageSaving(com.aspose.words.PageSavingArgs)](../../com.aspose.words/ipagesavingcallback\#pageSaving-com.aspose.words.PageSavingArgs-)事件。

要了解更多信息，请访问**Programming with Documents**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getKeepPageStreamOpen()](#getKeepPageStreamOpen--) | 指定 Aspose.Words 应该在保存文档页面后保持流打开还是关闭它。 |
| [getPageFileName()](#getPageFileName--) | 获取将保存文档页面的文件名。 |
| [getPageIndex()](#getPageIndex--) | 当前页面索引。 |
| [getPageStream()](#getPageStream--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setKeepPageStreamOpen(boolean value)](#setKeepPageStreamOpen-boolean-) | 指定 Aspose.Words 应该在保存文档页面后保持流打开还是关闭它。 |
| [setPageFileName(String value)](#setPageFileName-java.lang.String-) | 设置将保存文档页面的文件名。 |
| [setPageStream(OutputStream value)](#setPageStream-java.io.OutputStream-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getKeepPageStreamOpen() {#getKeepPageStreamOpen--}
```
public boolean getKeepPageStreamOpen()
```


指定 Aspose.Words 应该在保存文档页面后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.PageSavingArgs.PageStream**将文档页面写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**退货:**
boolean - 对应的布尔值。
### getPageFileName() {#getPageFileName--}
```
public String getPageFileName()
```


获取将保存文档页面的文件名。如果未指定，则将使用原始文件名自动生成页面文件名和路径。

**退货:**
java.lang.String - 文档页面将被保存到的文件名。
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


当前页面索引。

**退货:**
int - 对应的 int 值。
### getPageStream() {#getPageStream--}
```
public OutputStream getPageStream()
```




**退货:**
java.io.OutputStream
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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


指定 Aspose.Words 应该在保存文档页面后保持流打开还是关闭它。

默认为 false 并且 Aspose.Words 将关闭您在**P:Aspose.Words.Saving.PageSavingArgs.PageStream**将文档页面写入其中后的属性。指定 true 以保持流打开。

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPageFileName(String value) {#setPageFileName-java.lang.String-}
```
public void setPageFileName(String value)
```


设置将保存文档页面的文件名。如果未指定，则将使用原始文件名自动生成页面文件名和路径。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 将保存文档页面的文件名。 |

### setPageStream(OutputStream value) {#setPageStream-java.io.OutputStream-}
```
public void setPageStream(OutputStream value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
