---
title: Class RunCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.RunCollection 班级. 提供对集合的类型化访问Run节点.
type: docs
weight: 4570
url: /zh/net/aspose.words/runcollection/
---
## RunCollection class

提供对集合的类型化访问[`Run`](../run/)节点.

```csharp
public class RunCollection : NodeCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words/runcollection/item/) { get; } | 检索一个 **跑**在给定的索引处。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | 将一个节点添加到集合的末尾。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | 确定一个节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | 将一个节点插入到集合中指定索引处。 |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | 将集合中的所有运行复制到新的运行数组。 (2 methods) |

### 例子

显示如何确定内联节点的修订类型。

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// 当我们在编辑文档的同时出现“Track Changes”选项，在via Review ->中找到追踪，
// 在 Microsoft Word 中打开，我们应用的更改算作修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订
// 调用文档的“StartTrackRevisions”方法并使用“StopTrackRevisions”方法停止跟踪。
// 我们可以接受修订以将它们吸收到文档中
// 或拒绝它们以有效地更改提议的更改。
Assert.AreEqual(6, doc.Revisions.Count);

// 修订的父节点是修订所关注的运行。运行是一个内联节点。
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// 以下是可以标记内联节点的五种类型的修订。
// 1 - “插入”修订：
// 当我们在跟踪更改时插入文本时会发生此修订。
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - “格式”修订：
// 当我们在跟踪更改时更改文本格式时会发生此修订。
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - “移动”版本：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖到文档中的不同位置时
// 在跟踪更改时，会出现两个修订。
// “移动”版本是我们移动之前文本的副本。
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - “移至”修订版：
// “移动到”修订版是我们在文档中移动到其新位置的文本。
// 对于我们执行的每个移动修订，“从”和“移动到”修订成对出现。
// 接受移动修订删除“移动”修订及其文本，
// 并保留“移至”修订版中的文本。
// 拒绝移动修订相反地保留“移动”修订并删除“移动到”修订。
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - “删除”修订：
// 当我们在跟踪更改时删除文本时会发生此修订。当我们删除这样的文本时，
// 它将作为修订保留在文档中，直到我们接受修订，
// 这将永久删除文本，或者拒绝修订，这将使我们删除的文本保持在原来的位置。
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### 也可以看看

* class [NodeCollection](../nodecollection/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


