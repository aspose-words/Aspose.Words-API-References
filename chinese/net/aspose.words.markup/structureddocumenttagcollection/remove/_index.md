---
title: StructuredDocumentTagCollection.Remove
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTagCollection 方法. 删除具有指定标识符的结构化文档标签
type: docs
weight: 70
url: /zh/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

删除具有指定标识符的结构化文档标签。

```csharp
public void Remove(int id)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| id | Int32 | 结构化文档标签标识符。 |

### 例子

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
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* 部件 [Aspose.Words](../../../)


