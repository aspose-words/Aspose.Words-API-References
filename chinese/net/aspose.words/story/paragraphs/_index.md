---
title: Story.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words for .NET
description: 发现故事段落。直接从您的故事中访问精选的段落集合，以丰富、引人入胜的内容增强您的叙述。
type: docs
weight: 30
url: /zh/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

获取故事的直接子段落集合。

```csharp
public ParagraphCollection Paragraphs { get; }
```

## 例子

展示如何检查某个段落是否为移动修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// 本文档包含“移动”修订，当我们用光标突出显示文本时，这些修订就会出现，
// 然后拖动它以将其移动到另一个位置
// 同时通过“审阅”->“跟踪更改”在 Microsoft Word 中跟踪修订。
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // 移动修订由“移动自”和“移动到”修订对组成。
// 这些修订是文档的潜在更改，我们可以接受或拒绝。
// 在我们接受/拒绝移动修订之前，文档
// 必须跟踪文本的出发和到达目的地。
// 第二段和第四段定义了一个这样的修订，因此两者具有相同的内容。
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// “从中移动”修订版是我们从中拖动文本的段落。
// 如果我们接受修改，此段落将会消失，
// 另一个将保留并且不再是修订版。
Assert.True(paragraphs[1].IsMoveFromRevision);

// “移动到”修订版是我们将文本拖到的段落。
// 如果我们拒绝修改，则此段落将会消失，而另一段落将保留。
Assert.True(paragraphs[3].IsMoveToRevision);
```

### 也可以看看

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
