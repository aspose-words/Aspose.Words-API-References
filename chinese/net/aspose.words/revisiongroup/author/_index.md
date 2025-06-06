---
title: RevisionGroup.Author
linktitle: Author
articleTitle: Author
second_title: Aspose.Words for .NET
description: 发现 RevisionGroup Author 属性可以轻松识别每个修订组的作者，从而提高您的文档管理效率。
type: docs
weight: 10
url: /zh/net/aspose.words/revisiongroup/author/
---
## RevisionGroup.Author property

获取此修订组的作者。

```csharp
public string Author { get; }
```

## 例子

展示如何打印有关文档中一组修订的信息。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### 也可以看看

* class [RevisionGroup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
