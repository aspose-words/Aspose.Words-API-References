---
title: NodeChangingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for methods of the  interface.
type: docs
weight: 406
url: /java/com.aspose.words/nodechangingargs/
---

**Inheritance:**
java.lang.Object
```
public class NodeChangingArgs
```

Provides data for methods of the [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) interface.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAction()](#getAction) | Gets a value indicating what type of node change event is occurring. |
| [getClass()](#getClass) |  |
| [getNewParent()](#getNewParent) | Gets the node's parent that will be set after the operation completes. |
| [getNode()](#getNode) | Gets the [getNode()](../../com.aspose.words/nodechangingargs\#getNode) that is being added or removed. |
| [getOldParent()](#getOldParent) | Gets the node's parent before the operation began. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAction() {#getAction}
```
public int getAction()
```


Gets a value indicating what type of node change event is occurring.

**Returns:**
int - A value indicating what type of node change event is occurring. The returned value is one of [NodeChangingAction](../../com.aspose.words/nodechangingaction) constants.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getNewParent() {#getNewParent}
```
public Node getNewParent()
```


Gets the node's parent that will be set after the operation completes.

**Returns:**
[Node](../../com.aspose.words/node) - The node's parent that will be set after the operation completes.
### getNode() {#getNode}
```
public Node getNode()
```


Gets the [getNode()](../../com.aspose.words/nodechangingargs\#getNode) that is being added or removed.

**Returns:**
[Node](../../com.aspose.words/node) - The [getNode()](../../com.aspose.words/nodechangingargs\#getNode) that is being added or removed.
### getOldParent() {#getOldParent}
```
public Node getOldParent()
```


Gets the node's parent before the operation began.

**Returns:**
[Node](../../com.aspose.words/node) - The node's parent before the operation began.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

