---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: 用于 .NET 的 Aspose.Words
description: RevisionCollection AcceptAll 方法. 接受此集合中的所有修订 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

接受此集合中的所有修订。

```csharp
public void AcceptAll()
```

## 例子

显示如何比较文档。

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// 比较文档和修订版本会抛出异常。
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// 比较后，原文档会得到一个新的修订版
// 对于已编辑文档中不同的每个元素。
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
