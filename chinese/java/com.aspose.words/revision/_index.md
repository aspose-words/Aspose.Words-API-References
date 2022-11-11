---
title: Revision
second_title: Aspose.Words for Java API 参考
description:表示文档节点或样式中的修订跟踪更改。
type: docs
weight: 483
url: /zh/java/com.aspose.words/revision/
---

**遗产:**
java.lang.Object
```
public class Revision
```

表示文档节点或样式中的修订（跟踪更改）。利用[getRevision类型()](../../com.aspose.words/revision\#getRevision类型--)检查此修订的类型。

要了解更多信息，请访问**Track Changes in a Document**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [accept()](#accept--) | 接受此修订。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAuthor()](#getAuthor--) | 获取此修订的作者。 |
| [get班级()](#get班级--) |  |
| [getDateTime()](#getDateTime--) | 获取此修订的日期/时间。 |
| [getGroup()](#getGroup--) | 获取修订组。 |
| [getParentNode()](#getParentNode--) | 获取此修订的直接父节点（所有者）。 |
| [getParentStyle()](#getParentStyle--) | 获取此修订的直接父样式（所有者）。 |
| [getRevision类型()](#getRevision类型--) | 获取此修订的类型。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [reject()](#reject--) | 拒绝此修订。 |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | 设置此修订的作者。 |
| [setDateTime(Date value)](#setDateTime-java.util.Date-) | 设置此修订的日期/时间。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept() {#accept--}
```
public void accept()
```


接受此修订。

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
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


获取此修订的作者。不能为空字符串或 null。

**退货:**
java.lang.String - 此版本的作者。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDateTime() {#getDateTime--}
```
public Date getDateTime()
```


获取此修订的日期/时间。

**退货:**
java.util.Date - 本次修订的日期/时间。
### getGroup() {#getGroup--}
```
public RevisionGroup getGroup()
```


获取修订组。如果修订不属于任何组，则返回 null。如果修订类型为 Revision类型.StyleDefinitionChange 或如果修订不再存在于文档上下文中（接受/拒绝），则修订没有组。

**退货:**
[RevisionGroup](../../com.aspose.words/revisiongroup) - 修订组。
### getParentNode() {#getParentNode--}
```
public Node getParentNode()
```


获取此修订的直接父节点（所有者）。此属性适用于除[Revision类型.STYLE\_DEFINITION\_CHANGE](../../com.aspose.words/revisiontype\#STYLE-DEFINITION-CHANGE).如果此修订涉及样式格式的更改，请使用[getParentStyle()](../../com.aspose.words/revision\#getParentStyle--)反而。

**退货:**
[Node](../../com.aspose.words/node) - 此修订的直接父节点（所有者）。
### getParentStyle() {#getParentStyle--}
```
public Style getParentStyle()
```


获取此修订的直接父样式（所有者）。此属性仅适用于[Revision类型.STYLE\_DEFINITION\_CHANGE](../../com.aspose.words/revisiontype\#STYLE-DEFINITION-CHANGE)修订类型。如果此修订涉及文档节点上的更改，请使用[getParentNode()](../../com.aspose.words/revision\#getParentNode--)反而。

**退货:**
[Style](../../com.aspose.words/style) 此修订的直接父样式（所有者）。
### getRevision类型() {#getRevision类型--}
```
public int getRevision类型()
```


获取此修订的类型。

**退货:**
 int - 此修订的类型。返回值是以下之一[Revision类型](../../com.aspose.words/revisiontype)常数。
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




### reject() {#reject--}
```
public void reject()
```


拒绝此修订。

### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


设置此修订的作者。不能为空字符串或 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 本次修订的作者。 |

### setDateTime(Date value) {#setDateTime-java.util.Date-}
```
public void setDateTime(Date value)
```


设置此修订的日期/时间。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 本次修订的日期/时间。 |

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
