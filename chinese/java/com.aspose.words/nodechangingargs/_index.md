---
title: NodeChangingArgs
second_title: Aspose.Words for Java API 参考
description: 为接口的方法提供数据。
type: docs
weight: 403
url: /zh/java/com.aspose.words/nodechangingargs/
---

**遗产:**
java.lang.Object
```
public class NodeChangingArgs
```

为方法提供数据[INodeChangingCallback](../../com.aspose.words/inodechangingcallback)界面。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAction()](#getAction--) | 获取一个值，该值指示正在发生什么类型的节点更改事件。 |
| [getClass()](#getClass--) |  |
| [getNewParent()](#getNewParent--) | 获取将在操作完成后设置的节点的父节点。 |
| [getNode()](#getNode--) | 获取[getNode()](../../com.aspose.words/nodechangingargs\#getNode--)正在添加或删除。 |
| [getOldParent()](#getOldParent--) | 在操作开始之前获取节点的父节点。 |
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
### getAction() {#getAction--}
```
public int getAction()
```


获取一个值，该值指示正在发生什么类型的节点更改事件。

**退货:**
 int - 指示正在发生什么类型的节点更改事件的值。返回值是以下之一[NodeChangingAction](../../com.aspose.words/nodechangingaction)常数。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getNewParent() {#getNewParent--}
```
public Node getNewParent()
```


获取将在操作完成后设置的节点的父节点。

**退货:**
[Node](../../com.aspose.words/node) 操作完成后将设置的节点的父节点。
### getNode() {#getNode--}
```
public Node getNode()
```


获取[getNode()](../../com.aspose.words/nodechangingargs\#getNode--)正在添加或删除。

**退货:**
[Node](../../com.aspose.words/node) - 这[getNode()](../../com.aspose.words/nodechangingargs\#getNode--)正在添加或删除。
### getOldParent() {#getOldParent--}
```
public Node getOldParent()
```


在操作开始之前获取节点的父节点。

**退货:**
[Node](../../com.aspose.words/node) - 操作开始前节点的父节点。
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
