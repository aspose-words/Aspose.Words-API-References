---
title: INodeChangingCallback
linktitle: INodeChangingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to receive notifications when nodes are inserted or removed in the document in Java.
type: docs
weight: 659
url: /java/com.aspose.words/inodechangingcallback/
---
```
public interface INodeChangingCallback
```

Implement this interface if you want to receive notifications when nodes are inserted or removed in the document.
## Methods

| Method | Description |
| --- | --- |
| [nodeInserted(NodeChangingArgs args)](#nodeInserted-com.aspose.words.NodeChangingArgs) | Called when a node belonging to this document has been inserted into another node. |
| [nodeInserting(NodeChangingArgs args)](#nodeInserting-com.aspose.words.NodeChangingArgs) | Called just before a node belonging to this document is about to be inserted into another node. |
| [nodeRemoved(NodeChangingArgs args)](#nodeRemoved-com.aspose.words.NodeChangingArgs) | Called when a node belonging to this document has been removed from its parent. |
| [nodeRemoving(NodeChangingArgs args)](#nodeRemoving-com.aspose.words.NodeChangingArgs) | Called just before a node belonging to this document is about to be removed from the document. |
### nodeInserted(NodeChangingArgs args) {#nodeInserted-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeInserted(NodeChangingArgs args)
```


Called when a node belonging to this document has been inserted into another node.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

### nodeInserting(NodeChangingArgs args) {#nodeInserting-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeInserting(NodeChangingArgs args)
```


Called just before a node belonging to this document is about to be inserted into another node.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

### nodeRemoved(NodeChangingArgs args) {#nodeRemoved-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeRemoved(NodeChangingArgs args)
```


Called when a node belonging to this document has been removed from its parent.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

### nodeRemoving(NodeChangingArgs args) {#nodeRemoving-com.aspose.words.NodeChangingArgs}
```
public abstract void nodeRemoving(NodeChangingArgs args)
```


Called just before a node belonging to this document is about to be removed from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs/) |  |

