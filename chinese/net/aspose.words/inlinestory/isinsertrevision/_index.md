---
title: InlineStory.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words for .NET
description: 探索 InlineStory 的 IsInsertRevision 属性。启用更改跟踪功能，轻松识别 Word 中插入的对象。立即增强您的文档管理！
type: docs
weight: 40
url: /zh/net/aspose.words/inlinestory/isinsertrevision/
---
## InlineStory.IsInsertRevision property

如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。

```csharp
public bool IsInsertRevision { get; }
```

## 例子

展示如何查看 InlineStory 节点的修订相关属性。

```csharp
Document doc = new Document(MyDir + "Revision footnotes.docx");

// 当我们编辑文档时，可以通过“审阅”->“跟踪”找到“跟踪更改”选项，
// 在 Microsoft Word 中打开，我们应用的更改算作修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订
// 调用文档的“StartTrackRevisions”方法并使用“StopTrackRevisions”方法停止跟踪。
// 我们可以接受修订并将其融入文档
// 或者拒绝他们撤消并放弃提议的更改。
Assert.IsTrue(doc.HasRevisions);

List<Footnote> footnotes = doc.GetChildNodes(NodeType.Footnote, true).Cast<Footnote>().ToList();

Assert.AreEqual(5, footnotes.Count);

// 以下是五种可以标记 InlineStory 节点的修订类型。
// 1 - “插入”修订：
// 当我们在跟踪更改时插入文本时会发生此修订。
Assert.IsTrue(footnotes[2].IsInsertRevision);

// 2 - “移出”修订：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档中的其他位置时
// 跟踪更改时，出现两个修订版本。
// “移动自”修订版是我们移动它之前的原始文本的副本。
Assert.IsTrue(footnotes[4].IsMoveFromRevision);

// 3 – “移至”修订：
// “移动到”修订版是我们将文本移动到文档中的新位置。
// 我们执行的每次移动修订中，“从...移动”和“移动到...修订”都会成对出现。
// 接受移动修订将删除“移动自”修订及其文本，
// 并保留“移至”修订版中的文本。
// 拒绝移动修订则相反地保留“移动自”修订并删除“移动到”修订。
Assert.IsTrue(footnotes[1].IsMoveToRevision);

// 4 - “删除”修订：
// 当我们在跟踪更改时删除文本时，会发生此修订。当我们删除这样的文本时，
// 它将作为修订版本保留在文档中，直到我们接受该修订版本，
// 这将永久删除文本，或拒绝修订，这将保留我们删除的文本原位。
Assert.IsTrue(footnotes[3].IsDeleteRevision);
```

### 也可以看看

* class [InlineStory](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
