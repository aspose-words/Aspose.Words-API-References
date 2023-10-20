---
title: RevisionGroupCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: 用于 .NET 的 Aspose.Words
description: RevisionGroupCollection GetEnumerator 方法. 返回一个枚举器对象 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/revisiongroupcollection/getenumerator/
---
## RevisionGroupCollection.GetEnumerator method

返回一个枚举器对象。

```csharp
public IEnumerator<RevisionGroup> GetEnumerator()
```

## 例子

展示如何使用文档的修订集合。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// 这个集合本身有一个修订组的集合。
// 每组是相邻修订的序列。
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// 遍历组的集合并打印修订所涉及的文本。
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// 修订影响的每个运行都会获得一个相应的修订对象。
// 修订版的集合比我们上面打印的压缩形式大得多，
// 取决于我们在 Microsoft Word 编辑期间将文档分割成多少次运行。
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange 严格影响样式而不是文档节点。这意味着“父母风格”
        // 属性将始终处于使用状态，而 ParentNode 将始终为空。
        // 由于所有其他更改都会影响节点，因此 ParentNode 将反过来被使用，并且 ParentStyle 将为 null。
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

// 通过集合拒绝所有修订，将文档恢复为原始形式。
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### 也可以看看

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
