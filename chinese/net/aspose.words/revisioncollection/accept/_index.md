---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: 探索 RevisionCollection Accept 方法，根据您的标准轻松管理和过滤修订，从而简化项目更新。
type: docs
weight: 40
url: /zh/net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

接受符合指定条件的修订。

```csharp
public int Accept(IRevisionCriteria criteria)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| criteria | IRevisionCriteria | [`IRevisionCriteria`](../../irevisioncriteria/)实施. |

### 返回值

已接受修订的数量。

## 例子

显示如何根据标准接受或拒绝修订。

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // 要将我们的编辑注册为修订，我们需要声明一个作者，然后开始跟踪它们。
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // 删除运行“这不算作修订。”。
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // 我们有两个来自不同作者的修订版本，因此我们只需要接受一个。
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // 拒绝作者姓名和修订类型不同的修订。
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// 控制何时接受/拒绝某些修订。
/// </summary>
public class RevisionCriteria : IRevisionCriteria
{
    private readonly string AuthorName;
    private readonly RevisionType RevisionType;

    public RevisionCriteria(string authorName, RevisionType revisionType)
    {
        AuthorName = authorName;
        RevisionType = revisionType;
    }

    public bool IsMatch(Revision revision)
    {
        return revision.Author == AuthorName && revision.RevisionType == RevisionType;
    }
}
```

### 也可以看看

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
