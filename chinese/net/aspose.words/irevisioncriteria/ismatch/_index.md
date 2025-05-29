---
title: IRevisionCriteria.IsMatch
linktitle: IsMatch
articleTitle: IsMatch
second_title: Aspose.Words for .NET
description: 了解 IRevisionCriteria IsMatch 方法如何有效验证特定修订是否符合您的标准以获得最佳结果。
type: docs
weight: 10
url: /zh/net/aspose.words/irevisioncriteria/ismatch/
---
## IRevisionCriteria.IsMatch method

检查是否指定*revision*符合条件。

```csharp
public bool IsMatch(Revision revision)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revision | Revision | 这[`Revision`](../../revision/)实例来匹配标准。 |

### 返回值

`真的`如果*revision*符合条件，否则`错误的`。

## 评论

方法实现不应接受/拒绝修订或由于意外结果以任何方式修改它。

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

* class [Revision](../../revision/)
* interface [IRevisionCriteria](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
