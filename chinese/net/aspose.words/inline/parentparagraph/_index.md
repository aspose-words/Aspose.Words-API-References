---
title: Inline.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words for .NET
description: 发现 Inline ParentParagraph 属性可以轻松访问任何节点的父段落，从而提高您的编码效率和结构。
type: docs
weight: 70
url: /zh/net/aspose.words/inline/parentparagraph/
---
## Inline.ParentParagraph property

检索父级[`Paragraph`](../../paragraph/)此节点的。

```csharp
public Paragraph ParentParagraph { get; }
```

## 例子

展示如何确定内联节点的修订类型。

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// 当我们编辑文档时，可以通过“审阅”->“跟踪”找到“跟踪更改”选项，
// 在 Microsoft Word 中打开，我们应用的更改算作修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订
// 调用文档的“StartTrackRevisions”方法并使用“StopTrackRevisions”方法停止跟踪。
// 我们可以接受修订并将其融入文档
// 或拒绝他们以有效地更改所提议的变更。
Assert.AreEqual(6, doc.Revisions.Count);

// 修订的父节点是该修订所涉及的运行。运行是一个内联节点。
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// 以下是五种可以标记内联节点的修订类型。
// 1 - “插入”修订：
// 当我们在跟踪更改时插入文本时会发生此修订。
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - “格式”修订：
// 当我们在跟踪更改的同时更改文本的格式时，就会发生此修订。
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - “移出”修订：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档中的其他位置时
// 跟踪更改时，出现两个修订版本。
// “移动自”修订版是我们移动它之前的原始文本的副本。
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 – “移至”修订：
// “移动到”修订版是我们将文本移动到文档中的新位置。
// 我们执行的每次移动修订中，“从...移动”和“移动到...修订”都会成对出现。
// 接受移动修订将删除“移动自”修订及其文本，
// 并保留“移至”修订版中的文本。
// 拒绝移动修订则相反地保留“移动自”修订并删除“移动到”修订。
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - “删除”修订：
// 当我们在跟踪更改时删除文本时，会发生此修订。当我们删除这样的文本时，
// 它将作为修订版本保留在文档中，直到我们接受该修订版本，
// 这将永久删除文本，或拒绝修订，这将保留我们删除的文本原位。
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### 也可以看看

* class [Paragraph](../../paragraph/)
* class [Inline](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
