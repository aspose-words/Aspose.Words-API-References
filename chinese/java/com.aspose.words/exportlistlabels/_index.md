---
title: ExportListLabels
second_title: Aspose.Words for Java API 参考
description: 指定如何将列表标签导出为 HTML MHTML 和 EPUB。
type: docs
weight: 150
url: /zh/java/com.aspose.words/exportlistlabels/
---

**遗产:**
java.lang.Object
```
public class ExportListLabels
```

指定如何将列表标签导出为 HTML、MHTML 和 EPUB。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AS_INLINE_TEXT](#AS-INLINE-TEXT) | 将所有列表标签输出为内联文本。 |
| [AUTO](#AUTO) | 在自动模式下输出列表标签。 |
| [BY_HTML_TAGS](#BY-HTML-TAGS) | 将所有列表标签输出为 HTML 原生元素。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String exportListLabelsName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int exportListLabels)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int exportListLabels)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AS_INLINE_TEXT {#AS-INLINE-TEXT}
```
public static int AS_INLINE_TEXT
```


将所有列表标签输出为内联文本。 HTML

tag 用于任何列表标签表示。

### AUTO {#AUTO}
```
public static int AUTO
```


在自动模式下输出列表标签。尽可能使用 HTML 原生元素。 HTML

 *  标签用于列表标签表示，如果它不会导致格式丢失，否则 HTML
    
    使用标签。

### BY_HTML_TAGS {#BY-HTML-TAGS}
```
public static int BY_HTML_TAGS
```


将所有列表标签输出为 HTML 原生元素。 HTML

 *  标签用于列表标签表示。一些格式丢失是可能的。

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
### fromName(String exportListLabelsName) {#fromName-java.lang.String-}
```
public static int fromName(String exportListLabelsName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| exportListLabelsName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int exportListLabels) {#getName-int-}
```
public static String getName(int exportListLabels)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| exportListLabels | int |  |

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
### toString(int exportListLabels) {#toString-int-}
```
public static String toString(int exportListLabels)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| exportListLabels | int |  |

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
