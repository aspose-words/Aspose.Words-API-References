---
title: RevisionGroup.RevisionType
second_title: Aspose.Words for .NET API 参考
description: RevisionGroup 财产. 获取该组中包含的修订类型
type: docs
weight: 20
url: /zh/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

获取该组中包含的修订类型。

```csharp
public RevisionType RevisionType { get; }
```

### 例子

显示如何在文档中打印有关一组修订的信息。

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
* 命名空间 [Aspose.Words](../../revisiongroup/)
* 部件 [Aspose.Words](../../../)


