---
title: RevisionCollection.AcceptAll
second_title: Aspose.Words for .NET API 参考
description: RevisionCollection 方法. 接受此集合中的所有修订
type: docs
weight: 40
url: /zh/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

接受此集合中的所有修订。

```csharp
public void AcceptAll()
```

### 例子

展示如何比较文档。

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// 将文档与修订版本进行比较将引发异常。
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// 对比后，原文档将获得新的修订版
// 对于编辑文档中每个不同的元素。
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// 接受这些修订会将原始文档转换为编辑后的文档。
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### 也可以看看

* class [RevisionCollection](../)
* 命名空间 [Aspose.Words](../../revisioncollection/)
* 部件 [Aspose.Words](../../../)


