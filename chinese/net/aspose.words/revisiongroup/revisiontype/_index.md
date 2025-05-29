---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words for .NET
description: 探索 RevisionGroup 和 RevisionType 属性，轻松识别和管理项目中的修订类型。立即简化您的工作流程！
type: docs
weight: 20
url: /zh/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

获取此组中包含的修订类型。

```csharp
public RevisionType RevisionType { get; }
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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
