---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.RevisionGroupCollection 类，其特点是高效管理文档修订组，以增强编辑和协作。
type: docs
weight: 5530
url: /zh/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

的集合[`RevisionGroup`](../revisiongroup/)表示文档中修订组的对象。

要了解更多信息，请访问[跟踪文档中的修订](https://docs.aspose.com/words/net/track-changes-in-a-document/)文档文章。

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | 返回集合中的修订组数。 |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | 返回指定索引处的修订组。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | 返回一个枚举器对象。 |

## 评论

您不能直接创建此类的实例。使用[`Groups`](../revisioncollection/groups/) 属性获取文档中存在的修订组。

## 例子

展示如何获取文档中的一组修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
