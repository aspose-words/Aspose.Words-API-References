---
title: PageLayoutEvent
second_title: Aspose.Words for Java API Reference
description: 在页面布局模型构建和渲染期间引发的事件代码。
type: docs
weight: 436
url: /zh/java/com.aspose.words/pagelayoutevent/
---

**遗产:**
java.lang.Object
```
public class PageLayoutEvent
```

在页面布局模型构建和渲染期间引发的事件代码。

页面布局模型分两步构建。首先，“转换步骤”，这是页面布局拉取文档内容并创建对象图的时候。第二，“回流步骤”，这是结构被拆分、合并和排列成页面的时候。

根据触发构建的操作，页面布局模型可能会或可能不会进一步呈现为固定的页面格式。例如，计算文档中的页数或更新字段不需要渲染，而导出为 Pdf 则需要。
## 字段

| 字段 | 描述 |
| --- | --- |
| [BUILD_FINISHED](#BUILD-FINISHED) | 页面布局的构建已经完成。 |
| [BUILD_STARTED](#BUILD-STARTED) | 页面布局的构建已经开始。 |
| [CONVERSION_FINISHED](#CONVERSION-FINISHED) | 文档模型到页面布局的转换已完成。 |
| [CONVERSION_STARTED](#CONVERSION-STARTED) | 文档模型到页面布局的转换已经开始。 |
| [NONE](#NONE) | 默认值 |
| [PART_REFLOW_FINISHED](#PART-REFLOW-FINISHED) | 页面重排已完成。 |
| [PART_REFLOW_STARTED](#PART-REFLOW-STARTED) | 页面重排已开始。 |
| [PART_RENDERING_FINISHED](#PART-RENDERING-FINISHED) | 页面渲染完成。 |
| [PART_RENDERING_STARTED](#PART-RENDERING-STARTED) | 页面渲染已开始。 |
| [REFLOW_FINISHED](#REFLOW-FINISHED) | 页面布局的重排已完成。 |
| [REFLOW_STARTED](#REFLOW-STARTED) | 页面布局的重排已开始。 |
| [WATCH_DOG](#WATCH-DOG) | 对应于代码中经常被访问且适合中止进程的检查点。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pageLayoutEventName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int pageLayoutEvent)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pageLayoutEvent)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BUILD_FINISHED {#BUILD-FINISHED}
```
public static int BUILD_FINISHED
```


页面布局的构建已经完成。发射过一次。这是最后一次发生的事件[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)叫做。

### BUILD_STARTED {#BUILD-STARTED}
```
public static int BUILD_STARTED
```


页面布局的构建已经开始。发射过一次。这是第一个发生的事件[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)叫做。

### CONVERSION_FINISHED {#CONVERSION-FINISHED}
```
public static int CONVERSION_FINISHED
```


文档模型到页面布局的转换已完成。发射过一次。当布局模型停止提取文档内容时会发生这种情况。

### CONVERSION_STARTED {#CONVERSION-STARTED}
```
public static int CONVERSION_STARTED
```


文档模型到页面布局的转换已经开始。发射过一次。这发生在布局模型开始提取文档内容时。

### NONE {#NONE}
```
public static int NONE
```


默认值

### PART_REFLOW_FINISHED {#PART-REFLOW-FINISHED}
```
public static int PART_REFLOW_FINISHED
```


页面重排已完成。请注意，页面可能会多次重排，并且重排可能会在完成之前重新开始。

### PART_REFLOW_STARTED {#PART-REFLOW-STARTED}
```
public static int PART_REFLOW_STARTED
```


页面重排已开始。请注意，页面可能会多次重排，并且重排可能会在完成之前重新开始。

### PART_RENDERING_FINISHED {#PART-RENDERING-FINISHED}
```
public static int PART_RENDERING_FINISHED
```


页面渲染完成。每页触发一次。

### PART_RENDERING_STARTED {#PART-RENDERING-STARTED}
```
public static int PART_RENDERING_STARTED
```


页面渲染已开始。每页触发一次。

### REFLOW_FINISHED {#REFLOW-FINISHED}
```
public static int REFLOW_FINISHED
```


页面布局的重排已完成。发射过一次。当布局模型停止重排文档内容时会发生这种情况。

### REFLOW_STARTED {#REFLOW-STARTED}
```
public static int REFLOW_STARTED
```


页面布局的重排已开始。发射过一次。这发生在布局模型开始重排文档内容时。

### WATCH_DOG {#WATCH-DOG}
```
public static int WATCH_DOG
```


对应于代码中经常被访问且适合中止进程的检查点。

在里面的时候[IPageLayoutCallback.notify(com.aspose.words.PageLayoutCallbackArgs)](../../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-)抛出自定义异常以中止进程。

您可以在处理任何回调事件时抛出以中止进程。

请注意，如果进程中止，则页面布局模型仍处于未定义状态。但是，如果流程在整个页面的回流时中止，则应该可以使用布局模型直到该页面的末尾。

### length {#length}
```
public static int length
```


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
### fromName(String pageLayoutEventName) {#fromName-java.lang.String-}
```
public static int fromName(String pageLayoutEventName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageLayoutEventName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int pageLayoutEvent) {#getName-int-}
```
public static String getName(int pageLayoutEvent)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageLayoutEvent | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
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
### toString(int pageLayoutEvent) {#toString-int-}
```
public static String toString(int pageLayoutEvent)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pageLayoutEvent | int |  |

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
