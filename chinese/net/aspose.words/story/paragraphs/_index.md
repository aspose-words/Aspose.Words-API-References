---
title: Story.Paragraphs
second_title: Aspose.Words for .NET API 参考
description: Story 财产. 获取故事直接子级的段落集合
type: docs
weight: 30
url: /zh/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

获取故事直接子级的段落集合。

```csharp
public ParagraphCollection Paragraphs { get; }
```

### 例子

演示如何检查段落是否是移动修订。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// 该文档包含“移动”修订，当我们用光标突出显示文本时会出现该修订，
//然后拖动它以将其移动到另一个位置
// 在 Microsoft Word 中通过“审阅”跟踪修订时 -> “跟踪变化”。
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // 移动修订由成对的“移自”和“移至”修订组成。
// 这些修订是对文档的潜在更改，我们可以接受或拒绝。
// 在我们接受/拒绝移动修订之前，文档
// 必须跟踪文本的出发和到达目的地。
// 第二段和第四段定义了一个这样的修订，因此两者具有相同的内容。
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// “移自”修订版是我们拖动文本的段落。
// 如果我们接受修改，这一段就会消失，
// 另一个将保留并且不再是修订版。
Assert.True(paragraphs[1].IsMoveFromRevision);

// “移至”修订版是我们将文本拖动到的段落。
// 如果我们拒绝修改，则该段落将消失，而另一段将保留。
Assert.True(paragraphs[3].IsMoveToRevision);
```

### 也可以看看

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../story/)
* 部件 [Aspose.Words](../../../)


