---
title: NodeCollection.Clear
second_title: Aspose.Words for .NET API 参考
description: NodeCollection 方法. 从此集合和文档中删除所有节点
type: docs
weight: 40
url: /zh/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

从此集合和文档中删除所有节点。

```csharp
public void Clear()
```

### 例子

演示如何从文档中删除所有部分。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 该文档有一个部分，其中包含一些包含并显示文档所有内容的子节点。
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 清除节的集合，这将删除文档的所有子项。
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### 也可以看看

* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../nodecollection/)
* 部件 [Aspose.Words](../../../)


