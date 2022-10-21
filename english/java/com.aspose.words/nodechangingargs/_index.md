---
title: NodeChangingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for methods of the  interface.
type: docs
weight: 403
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
| [getNode()](#getNode--) | Gets the [getNode()](../../com.aspose.words/nodechangingargs\#getNode--) that is being added or removed. |
| [getOldParent()](#getOldParent--) | Gets the node's parent before the operation began. |
| [getNewParent()](#getNewParent--) | Gets the node's parent that will be set after the operation completes. |
| [getAction()](#getAction--) | Gets a value indicating what type of node change event is occurring. |
### getNode() {#getNode--}
```
public Node getNode()
```


Gets the [getNode()](../../com.aspose.words/nodechangingargs\#getNode--) that is being added or removed.

**Returns:**
[Node](../../com.aspose.words/node) - The [getNode()](../../com.aspose.words/nodechangingargs\#getNode--) that is being added or removed.
### getOldParent() {#getOldParent--}
```
public Node getOldParent()
```


Gets the node's parent before the operation began.

**Returns:**
[Node](../../com.aspose.words/node) - The node's parent before the operation began.
### getNewParent() {#getNewParent--}
```
public Node getNewParent()
```


Gets the node's parent that will be set after the operation completes.

**Returns:**
[Node](../../com.aspose.words/node) - The node's parent that will be set after the operation completes.
### getAction() {#getAction--}
```
public int getAction()
```


Gets a value indicating what type of node change event is occurring.

**Returns:**
int - A value indicating what type of node change event is occurring. The returned value is one of [NodeChangingAction](../../com.aspose.words/nodechangingaction) constants.
