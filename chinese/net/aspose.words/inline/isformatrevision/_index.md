---
title: Inline.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: 用于 .NET 的 Aspose.Words
description: Inline IsFormatRevision 财产. 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式则返回 true 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/inline/isformatrevision/
---
## Inline.IsFormatRevision property

如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。

```csharp
public bool IsFormatRevision { get; }
```

## 例子

演示如何确定内联节点的修订类型。

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// 当我们编辑文档的时候有“Track Changes”选项，在via Review中找到->追踪，
// 在 Microsoft Word 中打开，我们应用的更改算作修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订
// 调用文档的“StartTrackRevisions”方法并使用“StopTrackRevisions”方法停止跟踪。
// 我们可以接受修订以将它们吸收到文档中
// 或拒绝他们以有效地更改提议的更改。
Assert.AreEqual(6, doc.Revisions.Count);

// 修订版的父节点是该修订版涉及的运行。 Run 是一个内联节点。
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// 以下是可以标记内联节点的五种类型的修订。
// 1 - “插入”修订：
// 当我们在跟踪更改时插入文本时，会发生此修订。
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - “格式”修订：
// 当我们在跟踪更改的同时更改文本格式时，就会发生此修订。
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - “移自”修订版：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档中的其他位置时
// 跟踪更改时，会出现两个修订。
// “移自”修订版是我们移动文本之前的原始文本的副本。
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - “移动到”修订版：
// “移动到”修订版是我们移动到文档中新位置的文本。
// 对于我们执行的每个移动修订，“移动自”和“移动至”修订成对出现。
// 接受移动修订会删除“移动自”修订及其文本，
// 并保留“移至”修订版中的文本。
// 相反，拒绝移动修订会保留“移自”修订并删除“移至”修订。
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - “删除”修订版：
// 当我们在跟踪更改的同时删除文本时，会发生此修订。当我们删除这样的文本时，
// 它将作为修订版保留在文档中，直到我们接受修订版，
// 这将永久删除文本，或者拒绝修订，这将使我们删除的文本保留在原来的位置。
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### 也可以看看

* class [Inline](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
