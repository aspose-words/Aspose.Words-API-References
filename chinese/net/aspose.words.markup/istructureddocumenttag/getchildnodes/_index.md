---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words for .NET
description: 发现 IStructuredDocumentTag GetChildNodes 方法，访问根据您指定的类型定制的动态子节点集合，以增强文档管理。
type: docs
weight: 170
url: /zh/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

返回与指定类型匹配的子节点的实时集合。

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## 例子

展示如何删除结构化文档标签，但保留其中的内容。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // 此集合提供了用于访问范围和非范围结构化标签的统一接口。
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// 这里我们可以从范围和非范围结构化标签的公共接口中获取子节点。
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### 也可以看看

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
