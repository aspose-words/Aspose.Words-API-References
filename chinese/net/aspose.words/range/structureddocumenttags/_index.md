---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words for .NET
description: 发现 Range StructuredDocumentTags 属性，它提供了全面的结构化文档标签集合，增强了文档的组织和功能。
type: docs
weight: 50
url: /zh/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

返回`StructuredDocumentTags`表示范围内所有结构化文档标签的集合。

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## 例子

展示如何删除结构化文档标签。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// 通过 Id 删除结构化文档标签。
structuredDocumentTags.Remove(1691867797);
// 删除位置 0 处的结构化文档标签。
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### 也可以看看

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
