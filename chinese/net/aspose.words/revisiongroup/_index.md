---
title: Class RevisionGroup
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.RevisionGroup 班级. 代表一组顺序Revision对象.
type: docs
weight: 4780
url: /zh/net/aspose.words/revisiongroup/
---
## RevisionGroup class

代表一组顺序[`Revision`](../revision/)对象.

要了解更多信息，请访问[跟踪文档中的更改](https://docs.aspose.com/words/net/track-changes-in-a-document/)文档文章。

```csharp
public class RevisionGroup
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | 获取此修订组的作者。 |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | 获取此组中包含的修订类型。 |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | 返回插入/删除/移动的文本或格式更改的描述。 |

### 例子

演示如何打印有关文档中一组修订的信息。

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


