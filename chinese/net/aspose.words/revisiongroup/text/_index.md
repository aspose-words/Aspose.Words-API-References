---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 探索 RevisionGroup Text 属性以访问插入、删除或移动的文本，增强文档的格式洞察力和编辑效率。
type: docs
weight: 30
url: /zh/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

返回插入/删除/移动的文本或格式更改的描述。

```csharp
public string Text { get; }
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
