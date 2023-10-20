---
title: StructuredDocumentTagCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTagCollection RemoveAt 方法. 删除指定索引处的结构化文档标记 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

删除指定索引处的结构化文档标记。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 集合的索引。 |

## 例子

演示如何删除结构化文档标签。

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
// 通过Id删除结构化文档标签。
structuredDocumentTags.Remove(1691867797);
// 删除位置0处的结构化文档标签。
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### 也可以看看

* class [StructuredDocumentTagCollection](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
