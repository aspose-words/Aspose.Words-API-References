---
title: INodeChangingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您想在文档中插入或删除节点时接收通知，请实现此接口。
type: docs
weight: 652
url: /zh/java/com.aspose.words/inodechangingcallback/
---
```
public interface INodeChangingCallback
```

如果您想在文档中插入或删除节点时接收通知，请实现此接口。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [nodeInserted(NodeChangingArgs args)](#nodeInserted-com.aspose.words.NodeChangingArgs-) | 当属于此文档的节点已插入另一个节点时调用。 |
| [nodeInserting(NodeChangingArgs args)](#nodeInserting-com.aspose.words.NodeChangingArgs-) | 在属于该文档的节点即将插入另一个节点之前调用。 |
| [nodeRemoved(NodeChangingArgs args)](#nodeRemoved-com.aspose.words.NodeChangingArgs-) | 当属于此文档的节点已从其父节点中删除时调用。 |
| [nodeRemoving(NodeChangingArgs args)](#nodeRemoving-com.aspose.words.NodeChangingArgs-) | 在属于此文档的节点即将从文档中删除之前调用。 |
### nodeInserted(NodeChangingArgs args) {#nodeInserted-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeInserted(NodeChangingArgs args)
```


当属于此文档的节点已插入另一个节点时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |

### nodeInserting(NodeChangingArgs args) {#nodeInserting-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeInserting(NodeChangingArgs args)
```


在属于该文档的节点即将插入另一个节点之前调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |

### nodeRemoved(NodeChangingArgs args) {#nodeRemoved-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeRemoved(NodeChangingArgs args)
```


当属于此文档的节点已从其父节点中删除时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |

### nodeRemoving(NodeChangingArgs args) {#nodeRemoving-com.aspose.words.NodeChangingArgs-}
```
public abstract void nodeRemoving(NodeChangingArgs args)
```


在属于此文档的节点即将从文档中删除之前调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [NodeChangingArgs](../../com.aspose.words/nodechangingargs) |  |
