---
title: EditableRange
second_title: Aspose.Words for Java API 参考
description: 表示单个可编辑范围。
type: docs
weight: 136
url: /zh/java/com.aspose.words/editablerange/
---

**遗产：**
java.lang.Object
```
public class EditableRange
```

表示单个可编辑范围。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

[EditableRange](../../com.aspose.words/editablerange)是封装两个节点的“外观”对象[getEditableRangeStart()](../../com.aspose.words/editablerange\#getEditableRangeStart--)和[getEditableRangeEnd()](../../com.aspose.words/editablerange\#getEditableRangeEnd--)在文档树中，并允许将可编辑范围作为单个对象使用。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEditableRangeEnd()](#getEditableRangeEnd--) | 获取表示可编辑范围结束的节点。 |
| [getEditableRangeStart()](#getEditableRangeStart--) | 获取表示可编辑范围开始的节点。 |
| [getEditorGroup()](#getEditorGroup--) | 获取别名（或编辑组），用于确定是否允许当前用户编辑此可编辑范围。 |
| [getId()](#getId--) | 获取可编辑范围标识符。 |
| [getSingleUser()](#getSingleUser--) | 获取可编辑范围的单个用户。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除可编辑范围。 |
| [setEditorGroup(int value)](#setEditorGroup-int-) | 设置别名（或编辑组），用于确定是否允许当前用户编辑此可编辑范围。 |
| [setSingleUser(String value)](#setSingleUser-java.lang.String-) | 为可编辑范围设置单个用户。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getEditableRangeEnd() {#getEditableRangeEnd--}
```
public EditableRangeEnd getEditableRangeEnd()
```


获取表示可编辑范围结束的节点。

**退货：**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) - 表示可编辑范围结束的节点。
### getEditableRangeStart() {#getEditableRangeStart--}
```
public EditableRangeStart getEditableRangeStart()
```


获取表示可编辑范围开始的节点。

**退货：**
[EditableRangeStart](../../com.aspose.words/editablerangestart) - 表示可编辑范围开始的节点。
### getEditorGroup() {#getEditorGroup--}
```
public int getEditorGroup()
```


获取别名（或编辑组），用于确定是否允许当前用户编辑此可编辑范围。

特定可编辑范围不能同时设置单个用户和编辑组，如果设置了一个，另一个将被清除。

**退货：**
int - 别名（或编辑组），用于确定是否允许当前用户编辑此可编辑范围。返回值是其中之一[EditorType](../../com.aspose.words/editortype)常数。
### getId() {#getId--}
```
public int getId()
```


获取可编辑范围标识符。

该区域必须使用[getEditableRangeStart()](../../com.aspose.words/editablerange\#getEditableRangeStart--)和[getEditableRangeEnd()](../../com.aspose.words/editablerange\#getEditableRangeEnd--)

可编辑范围标识符应该在整个文档中是唯一的，Aspose.Words 在加载、保存和合并文档时自动维护可编辑范围标识符。

**退货：**
int - 可编辑范围标识符。
### getSingleUser() {#getSingleUser--}
```
public String getSingleUser()
```


获取可编辑范围的单个用户。

该编辑器可以以下列形式之一存储：

领域\\Username - 适用于其访问应使用当前用户的域凭据进行身份验证的用户。

user@domain.com - 适用于其访问应使用用户的电子邮件地址作为凭据进行身份验证的用户。

user - 对于其访问应使用当前用户的计算机凭据进行身份验证的用户。

特定可编辑范围不能同时设置单个用户和编辑组，如果设置了一个，另一个将被清除。

**退货：**
java.lang.String - 可编辑范围的单个用户。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public void remove()
```


从文档中删除可编辑范围。不删除可编辑范围内的内容。

### setEditorGroup(int value) {#setEditorGroup-int-}
```
public void setEditorGroup(int value)
```


设置别名（或编辑组），用于确定是否允许当前用户编辑此可编辑范围。

特定可编辑范围不能同时设置单个用户和编辑组，如果设置了一个，另一个将被清除。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 别名（或编辑组），用于确定是否允许当前用户编辑此可编辑范围。该值必须是其中之一[EditorType](../../com.aspose.words/editortype)常数。 |

### setSingleUser(String value) {#setSingleUser-java.lang.String-}
```
public void setSingleUser(String value)
```


为可编辑范围设置单个用户。

该编辑器可以以下列形式之一存储：

领域\\Username - 适用于其访问应使用当前用户的域凭据进行身份验证的用户。

user@domain.com - 适用于其访问应使用用户的电子邮件地址作为凭据进行身份验证的用户。

user - 对于其访问应使用当前用户的计算机凭据进行身份验证的用户。

特定可编辑范围不能同时设置单个用户和编辑组，如果设置了一个，另一个将被清除。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 可编辑范围的单个用户。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
