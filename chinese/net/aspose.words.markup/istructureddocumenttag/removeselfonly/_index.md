---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words for .NET
description: 发现 IStructuredDocumentTag RemoveSelfOnly 方法可以轻松删除 SDT 节点，同时在文档树中保留其内容。
type: docs
weight: 180
url: /zh/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

仅删除此 SDT 节点本身，但保留其在文档树中的内容。

```csharp
public void RemoveSelfOnly()
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

* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
