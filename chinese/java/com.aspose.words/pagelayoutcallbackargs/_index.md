---
title: PageLayoutCallbackArgs
second_title: Aspose.Words for Java API Reference
description: 传入的参数
type: docs
weight: 435
url: /zh/java/com.aspose.words/pagelayoutcallbackargs/
---

**遗产:**
java.lang.Object
```
public class PageLayoutCallbackArgs
```

传入的参数[IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-)

要了解更多信息，请访问**Converting to Fixed-page Format**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDocument()](#getDocument--) | 获取文档。 |
| [getEvent()](#getEvent--) | 获取事件。 |
| [getPageIndex()](#getPageIndex--) | 获取与此事件相关的文档中页面的从 0 开始的索引。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


获取文档。

**退货:**
[Document](../../com.aspose.words/document) - 文档。
### getEvent() {#getEvent--}
```
public int getEvent()
```


获取事件。

**退货:**
 int - 事件。返回值是以下之一[PageLayoutEvent](../../com.aspose.words/pagelayoutevent)常数。
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


获取与此事件相关的文档中页面的从 0 开始的索引。如果没有关联的页面，或者页面在回流期间被删除，则返回负值。

**退货:**
int - 与此事件相关的文档中页面的基于 0 的索引。
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
