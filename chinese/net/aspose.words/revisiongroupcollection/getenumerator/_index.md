---
title: RevisionGroupCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: 探索 RevisionGroupCollection GetEnumerator 方法——高效检索枚举器对象，以简化数据管理并增强性能。
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

展示如何处理文档的修订集合。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// 此集合本身具有修订组的集合。
// 每个组都是一系列相邻的修订版本。
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// 遍历组集合并打印修订所涉及的文本。
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// 修订影响的每个运行都会获得相应的修订对象。
// 修订的集合比我们上面打印的压缩形式要大得多，
// 取决于我们在 Microsoft Word 编辑期间将文档分割成多少个运行。
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange 严格影响样式，而不影响文档节点。这意味着“ParentStyle”
        // 属性将始终被使用，而 ParentNode 将始终为空。
        // 由于所有其他更改都会影响节点，因此 ParentNode 将相反地被使用，并且 ParentStyle 将为空。
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

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
