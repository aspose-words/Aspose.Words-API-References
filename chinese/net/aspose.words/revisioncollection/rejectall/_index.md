---
title: RevisionCollection.RejectAll
linktitle: RejectAll
articleTitle: RejectAll
second_title: 用于 .NET 的 Aspose.Words
description: RevisionCollection RejectAll 方法. 拒绝此集合中的所有修订 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/revisioncollection/rejectall/
---
## RevisionCollection.RejectAll method

拒绝此集合中的所有修订。

```csharp
public void RejectAll()
```

## 例子

展示如何使用文档的修订集合。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// 这个集合本身有一个修订组的集合。
// 每组都是相邻修订的序列。
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// 迭代组的集合并打印修订涉及的文本。
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// 修订影响的每个运行都会获取相应的修订对象。
// 修订的集合比我们上面打印的压缩形式要大得多，
// 取决于我们在 Microsoft Word 编辑期间将文档分段为多少次。
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange 严格影响样式而不是文档节点。这意味着“ParentStyle”
        // 属性将始终处于使用状态，而 ParentNode 将始终为 null。
        // 由于所有其他更改都会影响节点，因此 ParentNode 将相反地被使用，并且 ParentStyle 将为 null。
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// 通过集合拒绝所有修订，将文档恢复为其原始形式。
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### 也可以看看

* class [RevisionCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
