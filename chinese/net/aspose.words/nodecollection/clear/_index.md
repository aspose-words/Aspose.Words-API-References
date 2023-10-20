---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: 用于 .NET 的 Aspose.Words
description: NodeCollection Clear 方法. 从此集合和文档中删除所有节点 在 C#.
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

显示如何从文档中删除所有部分。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 此文档有一个部分，其中包含并显示所有文档的内容的几个子节点。
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 清除部分的集合，这将删除文档的所有子项。
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### 也可以看看

* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
