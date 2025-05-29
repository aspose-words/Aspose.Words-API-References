---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: 使用我们的 Clear 方法轻松清除您的 NodeCollection，从集合和文档中删除所有节点以获得最佳性能。
type: docs
weight: 40
url: /zh/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

从此集合和文档中删除所有节点。

```csharp
public void Clear()
```

## 例子

展示如何从文档中删除所有部分。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 该文档有一个部分，其中有几个子节点包含并显示文档的所有内容。
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 清除部分集合，这将删除文档的所有子部分。
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### 也可以看看

* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
